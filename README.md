To run on a VM with apache configure to serve a website from /var/www/html

$ sudo apt-get install ruby-full build-essential zlib1g-dev
$ echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
$ echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
$ echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
$ source ~/.bashrc
$ gem install jekyll bundler
$ sudo addgroup webeditor
$ sudo chown root:webeditor /var/www/html
$ sudo chmod g+w /var/www/html
$ sudo rm /var/www/html/index.html
$ sudo adduser ubuntu webeditor

disconnect and reconnect to your VM for new group to take affect.
$ git clone <this-repo> 
$ cd cloud_apps_in_hss
$ jekyll build -d /var/www/html/
