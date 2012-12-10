### Assumptions

* You have installed ruby, rails, vagrant, librarian

### Follow these steps to create a new rails app in vagrant box.

	git clone git@github.com:fungibleclouds/awesome_app.git 
	rails new ./awesome_app
	cd awesome_app
	mkdir site-cookbooks && cd site-cookbooks && touch README.md && cd ..
	# uncomment rails Gemfile to enable unicorn and therubyracer
	# add to Gemfile  gem 'libv8', '~> 3.11.8' 
	librarian-chef install
	vagrant up

open [awesome_app](http://33.33.33.10) to see it running on your vagrant box.
	