# Postmessage #

This is a sample that was first displayed in a YouTube video at https://www.youtube.com/watch?v=dvFfQ6rIH_A (pt.1) & https://www.youtube.com/watch?v=wc_tIlLkMso (pt.2)
It shows intra-process messaging with postmessage and inter-process message across a network via 2 methods.  
One uses a command line windows .exe program, the other uses the upostmsg.dll via a C signature.  
An extra form and startup shell interrogates URouters in the network, via the UROUTMON API, to find messaging targets.

## Dependencies ##

This sample has been written and tested with:

 * Uniface 10
 * The Setup instructions are specific to Uniface 10
 * SQLite

## Setup ##

 * This project can be downloaded using the WAS plugin (https://github.com/uniface/WASListener), compiled and run.
 * If you are not using the default urouter port 13001, please set as appropriate in the settings section of your ide / runtime assignment file using $DEFAULT_NET e.g.
   *  $DEFAULT_NET tcp:localhost+13002

 
## Contributing to the project ##
 
 * Verify that WASListener is syncing the Uniface repository with the WorkArea sub folder.
 * Make some changes in the repository and sync the WorkArea folder via the menu: 'WorkArea Export/Revert'
 * Use the git command line or your favourite tool to create pull requests.
