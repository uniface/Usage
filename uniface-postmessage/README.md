# Postmessage #

This is a sample that was first displayed in YouTube videos a few  years back.  
It shows intra-process messaging with postmessage and inter-process message (theoretically also across a network) via 2 methods.  
One uses a command line windows .exe program, the other uses the upostmsg.dll via a C signature.  
An extra form interrogates URouters in the network, via the UROUTMON API, to find messaging targets.

## Dependencies ##

Postmessage has been written and tested with:

 * Uniface 9.5 and 9.6.07 - if you wish to use the $processinfo function for creating a unique UST (based on PID), otherwise earlier versions can be used.
 * SQLite

## Setup ##

This project can be downloaded and setup in 2 ways. Either added to an existing Uniface project or setup standalone.

### Add Postmessage to an existing project ###
These instructions assume you're adding Postmessage to your default Uniface environment. Simply replace the paths with your own to add it to another project.

 * Download the latest zip from the downloads page
 * Copy Postmessage.uar to your project area (C:\\Users\\admin\\Documents\\Uniface 96 Development\\project)
 * Add a reference to Postmessage.uar in your idf.asn (C:\\Program Files (x86)\\Compuware\\Uniface 9.6\\uniface\\adm\\idf.asn). If you don't have a [resource] section, add one. In the resource section add the line C:\\Users\\admin\\Documents\\Uniface 96 Development\\project\\Postmessage.uar
 * Test with the UDE with /tst POSTMESS1 and /tst RECVMESS1

### Setup Postmessage as a standalone project ###
These instructions allow you to create a new stand alone project on your local machine. In order to clone the repository (download it to your machine) you will need a git client of some sort installed, something like [SourceTree](https://www.sourcetreeapp.com/).

 * For these steps you'll need the Project Setup Tool. Follow the instructions here https://bitbucket.org/uniface/project-setup-tool to setup this tool before continuing
 * Clone the Postmessage repository onto your local machine. For these steps we'll assume it's been cloned into C:\Projects\Postmessage
 * Open a command prompt in the root of the project and type "projectsetup" to invoke the Project Setup Tool. If your user doesn't have access rights to the directory that Uniface is installed in then you'll need to run the command prompt with administrator privileges.
 * Work through the setup process checking the details picked up by the setup tool make sense. Pay particular attention to user name and passwords.
 * Test with the UDE with /tst POSTMESS1 and /tst RECVMESS1
 
## Contributing to the project ##

To set up the project for development follow the steps above to create DSP Charts as a standalone project. Once complete the only other tool required is the Version Control project, allowing granular exports of source code suitable for use with BitBucket. To set this up follow these steps:

 * Visit https://bitbucket.org/uniface/version-control and follow the setup instructions to download the Version Control tool
 * Open the IDE and using the Utilities->Import menu import the file FILESYNC_Menu.xml. Assuming you extracted the Version Control tool to C:\\UnifacePackages, this would be found in C:\\UnifacePackages\\VersionControl\\imports
 * Compile the additional menu, which will in turn compile the menu we just imported
 * In the IDE go to Utilities->Preferences->General and tick the check box "Enable Additional Menu"
 * Now that the additional menu is enabled we can go to Utilities->Additional->Settings and using the browse button next to "Uniface Source Directory" select ./src. This points the tool at our source code.
 * Everything is now setup and we can go to Utilities->Additional->Project to verify that everything is setup correctly. Visiting this screen will sync your Uniface repository with the src folder. If it's working correctly then you should see the contents of this folder in the tree view.

## Contributors ##

* Eddy Knochs