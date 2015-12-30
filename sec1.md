# Section 1: Setting up the environment

For this tutorial, we'll be using Ubuntu 15.10, but you can use Windows if you'd like (but I won't be able to help you with this part for now).

After installing Ubuntu, you will need to run these commands. These download packages that will be used to setup the tools later. Some of these commands will ask you for your password.

    # Setup the computer to install Mono
    sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
    echo "deb http://download.mono-project.com/repo/debian wheezy main" | sudo tee /etc/apt/sources.list.d/mono-xamarin.list
    
    # Update the package list and install
    sudo apt-get update
    sudo apt-get install -y build-essential mono-complete
    
Once those have been run, you'll need to install devkitARM. This toolchain allows you to compile code for the 3DS's processor.

    wget "http://sourceforge.net/projects/devkitpro/files/Automated%20Installer/devkitARMupdate.pl/download" -o devkitARMupdate.pl
    sudo chmod +x devkitARMupdate.pl
    ./devkitARMupdate.pl

With that, you're ready to install the tools.

[Next section](sec2.md)
