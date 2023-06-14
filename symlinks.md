# Guide to symlinks

Symlinks allow you to create a "link" that you can use to call a function

## prereqs

create a file where all your symlinks are going to go

	mkdir bin
	
create a `/.bash_profile` if you dont already have one. Check to make sure you already have a `/.bashrc` file (you should)

	vim .bash_profile
		# .bash_profile                                                                                                                                        		# Get the aliases and functions
		if [ -f ~/.bashrc ]; then
			. ~/.bashrc
		fi
		# User specific environment and startup programs
		## path to your bin directory and local directory
		PATH=/home/brandon/bin:$PATH:$HOME/.local/bin:$HOME/bin
		
		export PATH
	
	# save and exit (press escape before you type below)
		:wq
		
now you have to reboot

	exec bash
	source ~/.bash_profile 
	bash

now go to the bin directory you created. this is where you will store your symlinks

	cd bin
	# create symlink
	ln -s ~/[path to igv] ./igv

this creates a shortcut to igv so it can be called by simply typing "igv" in the command line.