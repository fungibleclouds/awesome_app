### Assumptions

* You have installed ruby, rails, vagrant, librarian

### Follow these steps to create a new rails app in vagrant box.

    gem install librarian
	rails new awesome_app
	cd awesome_app
	wget https://raw.github.com/fungibleclouds/awesome_app/master/Cheffile
	wget https://raw.github.com/fungibleclouds/awesome_app/master/Vagrantfile
	mkdir site-cookbooks && cd site-cookbooks && touch README.md && cd ..
	# uncomment rails Gemfile to enable unicorn and therubyracer
	# edit .gitignore to ignore /cookbooks and Cheffile.lock and .vagrant
	
	librarian-chef install
	vagrant up

open [awesome_app](http://33.33.33.10) to see it running on your vagrant box.
	