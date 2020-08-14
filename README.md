# Postmessage #

This is a sample that was first displayed in YouTube videos a few  years back.  
It shows intra-process messaging with postmessage and inter-process message (theoretically also across a network) via 2 methods.  
One uses a command line windows .exe program, the other uses the upostmsg.dll via a C signature.  
An extra form and startup shell interrogates URouters in the network, via the UROUTMON API, to find messaging targets.

## Dependencies ##

Postmessage has been written and tested with:

 * Uniface 9.5 and 9.7.03 (9.6.07 and above if you wish to use the $processinfo function for creating a unique UST (based on PID))
 * The Setup instructions are specific to Uniface 9.7
 * SQLite

## Setup ##

This project can be downloaded and setup in 2 ways. Either as a new Uniface project without Version Control, or as a new project with Version Control.
Both setups use the Uniface Project Setup tooling.  Once the repository has been built with this tooling, the development objects can be exported using standard tools, or $ude, and then imported into an existing Uniface repository from another project.

 * Follow the instructions here https://github.com/uniface/Development-Tooling/tree/master/uniface-project-setup-tool to setup this tool before continuing.
 * Verify the setup tool.  Assuming it was installed to C:\\UnifacePackages, check that ProjectSetup97.bat is correct and matches the environment variables created.

### Setup Postmessage as a standalone project via Project Setup Tool ###

 * From GitHub, choose the Clone or Download button, and select download ZIP.
 * Open the ZIP file normally.  The uniface-structs folder can be ignored.  Extract the uniface-postmessage folder, or the contents with in to a location that meets your existing project needs, e.g. C:\\U9projects\\Postmessage
 * Start a DOS shell and cd to the project root folder, e.g. C:\\U9Projects\\Postmessage\\
 * Run the bat file projectsetup97. Work through the setup process checking the details picked up by the setup tool make sense. Pay particular attention to user name and passwords.
 * Shortcuts will appear in the project root folder.  Test with the UDE with /tst POSTMESS1 and /tst RECVMESS1.  Then start the Postmessage App shortcut.  

### Setup Postmessage as a standalone project with Version Control###
These instructions allow you to create a new stand alone project on your local machine. In order to clone the repository (download it to your machine) you will need a git client of some sort installed, something like [SourceTree](https://www.sourcetreeapp.com/).

 * Visit https://github.com/uniface/Development-Tooling/tree/master/uniface-version-control and follow the setup instructions to download the Version Control tool
 * Clone the Postmessage repository onto your local machine. For these steps we'll assume it's been cloned into C:\\U9Projects\\Postmessage
 * Start a DOS shell and cd to the project root folder, e.g. C:\\U9Projects\\Postmessage\\
 * Run the bat file projectsetup97. Work through the setup process checking the details picked up by the setup tool make sense. Pay particular attention to user name and passwords.
 * Shortcuts will appear in the project root folder.  Test with the UDE with /tst POSTMESS1 and /tst RECVMESS1.  Then start the Postmessage App shortcut.  
 
## Contributing to the project ##
 
 * Verify that VC is syncing the Uniface repository with the src sub folder.  Make some changes in the repository and sync the working folder via the menu: Utilities -> Additional -> File Sync -> Project.  You should see file timestamps changing, and unstaged files inside SourceTree.
 * Choose the files to stage, and then commit them to your local Master repo.
 * Further instructions to push these commits will be advised separately.

## Contributors ##

* Eddy Knochs
