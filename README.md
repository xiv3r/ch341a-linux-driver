# CH341A linux driver 
| debian | ubuntu | mint | kali | parrot |


# Install Dependencies:

    sudo -i
    sudo apt update
    sudo apt install bc build-essential
    sudo apt install linux-image-$(uname -r|sed 's,[^-]*-[^-]*-,,')
    sudo apt install linux-headers-$(uname -r|sed 's,[^-]*-[^-]*-,,')


# Description:

   USB serial driver for USB to UART chip ch340, ch341, etc. In fact Linux mainline kernels have built-in ch341 serial driver since kernel version 2.6.24 up to 6.6.15, The location is: drivers/usb/serial/ch341.c, it's a pity that the built-in driver cannot be kept up to date. We suggest our customers to use this driver.

# Setup:
Open root 'Terminal'
    
    sudo -i
    git clone https://github.com/xiv3r/ch341a-linux-driver.git
    cd ch341a-linux-driver

# Install drivers:
  
    sudo make ; sudo make load ; sudo make install


# Uninstall driver:

    sudo make unload ; sudo make uninstall

    
    
