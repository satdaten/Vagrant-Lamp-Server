This is an extension of the Vagrant (http://vagrantup.com/) getting started script. This script uses the Chef solo daemon to install a basic lamp stack with php debugging. As such, the idea is that this is for development.

What it does:

- install all needed package on Ubuntu Lucid Lynx x86
- Move over configuration files to make your root folder the root of the web server
- Move over a php.ini file so that debugging is turned on and errors are displayed to the screen.
- Set the mysql root password to "test"

What it does NOT do:

- Install any kind of SQL databases. That is all up to up.
- Create any users besides the vagrant default user
- Secure your server so that it is "production ready." As such, don't take the Chef cookbooks and deploy this to a production environment. 

CREDIT

All the cookbooks come from the Chef community (http://community.opscode.com/). I just modified a few files in there to make it work as a unified install outside of the default lamp cookbook they have.