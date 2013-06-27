launchvv
========

helper app for OS X to launch virt-viewer files from a browser


launchvv.script is an applescript application that enables seamless launching of spice consoles from RHEV 3.2 +.

What it actually does:
  
it reads the vv file received from RHEV  
extracts the hostname of the RHEV-M server  
checks to see if there is a CA certificate for that host in /tmp  
if not, it downloads the CA crt  
Finally it launches remote viewer with the appropriate CA cert and .vv file parameters.  
  
To use:  
  
Download the binary (launchvv.app) (select launch.vv, view raw) and place in /Applications  
Run it once to 'bless' the file with gatekeeper (it will do nothing).  
In the user or admin portal, set the console type to 'native'  
Click Console.  When your browser asks what to do with the file, associate it permanently with launchvv.  

