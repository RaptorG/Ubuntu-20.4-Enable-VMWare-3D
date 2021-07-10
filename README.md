# Ubuntu-20.4-Enable-VMWare-3D

# Enable 3D Hardware graphics acceleration for VMWare Workstation on Ubuntu

# Test3D Hardware graphic acceleration is enable on Ubuntu
# To test if 3D Hardware graphic acceleration is enable on Ubuntu, you will have to install mesa-utils

sudo apt-get install mesa-utils

# After you have mesa-utils installed, run glxinfo and look for “direct rendering” line (hardware acceleration)

sudo glxinfo | grep "direct rendering"

# If the output is “yes” then hardware acceleration is enabled already in your Ubuntu system.

# Enable 3D Hardware graphics acceleration for VMWare Workstation globally

$ sudo nano /etc/vmware/config

# Add the same line to the end of vmware global configure file

mks.gl.allowBlacklistedDrivers = TRUE

# Enable 3D Hardware graphics acceleration for VMWare Workstation per Linux’s User

# Edit vmware’s preferences file for your specific Linux’s user, make sure the current working directory is at /home/yourusername (replace yourusername with your actual user name). You can check your current working directory by using pwd command

$ pwd

To change your current working directory (replace yourusername with your actual user name) & edit vmware’s preferences file

$ cd /home/yourusername



$ nano .vmware/preferences

# add this line to the end preferences file

mks.gl.allowBlacklistedDrivers = "TRUE"
