# ABB_Yumi
**INSTALLING SLP DISTRIBUTOR AND HANDLING LICENSE DISTRIBUTION**
Download SLP Distributor:
SLP Distributor is distributed with RobotStudio and can be found in the following directory: RobotStudio_x.zip\RobotStudio\Utilities\SLP Distributor\

Firewall Settings (TCP ports)
Web interface: 2468
Licensing: 8731
The installer opens these ports in the standard Windows Firewall, but any third-party firewall must be configured manually.

Activate a network license manually:

Open the SLP Distributior website: http://localhost:2468/web
Click on the Activation tab and then Manual Activation
Enter the activation key and click “Submit”
The request data should look like this:
–BEGIN REQUEST–xxxxxxxxxxxx-- END REQUEST –
Paste the request data in your favorite text editor and save it with the name and extension: request**.licreqx**
Upload the request data file(.licreqx) to: http://manualactivation.e.abb.com/
A download link will appear, hit it and save the license file .bin
Open up SLP Distributor and choose “Browse” under install License and choose the .bin file and hit install.
Reinstall SLP Distributor and flush licenses:

Make sure the clock is synchronized.
Download the latest SLP distributor version that is distributed with the RobotStudio.zip
Reinstall SLP distributor from the terminal: ‘install.cmd -uninstall’
Remove old keys: ‘install.cmd -obliterate’ (THIS WILL MAKE YOUR LICENSE INVALID!)
Install The new SLP distributor: ‘install.cmd -install’
