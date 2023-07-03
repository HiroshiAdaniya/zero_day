# Vagrant

This is a project that helps me better understand the cloning of repositories onto other machies other than the sandbox.

## 1. Virtual machine: Download and Installing

* download and install VirtualBox:
	then vagrant || wsl on a windows

### VAGRANT, follow these steps:

**NB!: During the installing process of vagrant, you might run into an error indecating that you might not have Microsoft Visual C++ 2019(or later) Redistributable package installed. Download it and then install it.

* After installing vagrant:
	As Admin, run windows powershell || command prompt
	vagrant init ubuntu/trusty64

This will create a file on your local system. navigate to the folder outside of powershell and edit the text within that file.

	under: config.vm.box="ubuntu/focal64"
	enter: config.vm.box_download_insecure=true

Once that is done.
	
	in powershell: vagrant ssh

this will start vagrant VM.

* If you have installed a WSL you can skip the steps above and move onto the next

## 2. Setting up your system

* once installed within your new terminal download:

	git
	emacs(optinal)
	vim/vi(this should already come with the VM)
	betty

* Create your repository in Github and a token that doesn't expire

* Go into your WSL or VM(Vagrant in powershell or terminal)
 
	update your basic info(username and email):
		- git config --global user.name "user name"
		- git comfig --global user.email "user email"
## 3. Cloning

* To initilize git so that you can clone your repository

	git init
 
This creates a file within the directory you are in so that cloning can take place.without initlizing git, the cloning wont work. You will notice that we also initilized vagrant the same way. it both creates files with the code that is needed to download data/clone.

	git clone https://token@github.com/username/repositoryName.git

This will clone your github repository. You can now add a README, add it, commit it and then push it.

