# Autoinstall T-Pot on Ubuntu 16.04.x (Customized)
This script will install [T-Pot 17.10](http://dtag-dev-sec.github.io/mediator/feature/2017/11/07/t-pot-17.10.html) on a fresh Ubuntu 16.04.x LTS (64bit). 

Successfully tested on vanilla Ubuntu 16.04.3 in VMware.

Choose Ubuntu 16.04.x 64bit as operating system. 
Check and meet the [system requirements](http://dtag-dev-sec.github.io/mediator/feature/2017/11/07/t-pot-17.10.html#requirements) 

So, clone the repository. Run as root. Enjoy.

    groupadd groupX
    useradd -g groupX -m userX
    passwd userX
    
Make sure you have your SSH key added to your account (~/.ssh/authorized_keys) 

    su - tpot
    ssh-keygen
    <enter passphase>
    cp .ssh/id_rsa.pub .ssh/authorized_keys
        
    git clone https://github.com/dtag-dev-sec/t-pot-autoinstall.git
    cd t-pot-autoinstall/
    sudo su
    ./install.sh

If you run into problems during installation it might be related to your hoster's custom Ubuntu update repositories. So far, we do not have a solution for this. 

Due to public demand, we added a non-interactive installation option. Just add the *username*, the *number referencing the edition* and the *password for web access* to the installation script, e.g.

	./install.sh ubuntu 2 myPassw0rd
		
will install the **Honeypot Only Edition** (2) for the user "ubuntu" and set the web access password to "myPassw0rd". 


	

	
