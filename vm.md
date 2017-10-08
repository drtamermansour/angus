# Start up an Ubuntu 16.04 instance in a vriual machine on your computer

1)	Download Ubuntu desktop
    https://www.ubuntu.com/download/desktop 
    
    a.	Click download button 
    
    b.	You do not need to pay money. Move all bars to $0 dollars
    
    c.	Click download and save the iso image to your desk
        
2)	Install the virtual box according to your operating system (download, double click, follow default instructions)

    a.	Windows: http://download.virtualbox.org/virtualbox/5.1.28/VirtualBox-5.1.28-117968-Win.exe 

    b.	Mac: http://download.virtualbox.org/virtualbox/5.1.28/VirtualBox-5.1.28-117968-OSX.dmg 

3)	Install extension back (download, double click, follow default instructions): http://download.virtualbox.org/virtualbox/5.1.28/Oracle_VM_VirtualBox_Extension_Pack-5.1.28-117968.vbox-extpack 

4)	Creating your first virtual machine

    a.	Run the virtual box application (In windows, you might need to run as administrator)
    
    b.	Click on the “New” button at the top of the VirtualBox Manager window. A wizard will pop up to guide you through setting up a new virtual machine (VM).

        i.	Name: myUbuntu16.04
        ii.	Type: Linux
        iii.	Version: Ubuntu (64-bit)

    c.	Follow the default instructions for RAM (mine is 4GB), virtual hard desk (mine is 10GB), type of file (VDI), Storage, Location and size. Click create 

    d.	Start your new machine

    e.	You will be asked for the optical derive. Choose the small folder icon and find the Ubuntu iso image you downloaded in step no 1. (You can use the main virtual box interface to clicking on the optical derive under storage tab and find the iso image)

    f.	Click install Ubuntu
    
    g.	Check yes for updates and third party software. 
    
    h.	Make sure 'Erase disk and install Ubuntu' option is selected and click 'Install Now' button.
        
    i.	Answer the couple next questions 
    
    j.	Finish installation: You will be asked to restart, just click the restart button. Then you will be asked to remove the installation drive and click enter, just click enter.
 
5)	Create a folder on your desktop and name it “shared_VM”. Add it to your virtualbox as a shared folder using the same name 
https://www.howtogeek.com/189974/how-to-share-your-computers-files-with-a-virtual-machine/
> note: select Auto-mount in the last step

6)	Run your VM, go to applications, run a terminal, and Now add your user to the vboxsf group:

        sudo usermod -aG vboxsf $(whoami) 

7)	Restart you VM and open new terminal 
