# Vagrant Setup Guild

## Prerequisites

### Ruby
download <a href='https://github.com/oneclick/rubyinstaller2/releases/download/RubyInstaller-2.6.6-1/rubyinstaller-devkit-2.6.6-1-x64.exe'>here</a>

### Vagrant
download <a href='https://www.vagrantup.com/'>here</a>

### Virtual Box
download <a href='https://www.virtualbox.org/wiki/Downloads'>here</a>

## Installation

1. Once all dependecies have been installed we need to set up the vagrant configuration. To do this we need to create a file named Vagrantfile, within the file add the follow lines of code:
`Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.10.100"
end`

2. When the Vagrantfile has been saved with the code given code run this next line of code:
`vagrant up`

3. This should create the VM, to check the status run:
`vagrant status`

4. The status should show the the status is running, now to access the VM by running:
`vagrant ssh`

5. To update packages run:
`sudo apt-get update`

6. Packges can be installed by using apt-get, to install nginx run:
`sudo apt-get install nginx`

7. To check if everything is working enter the VM IP in a browser which was added in the config in step 1 which is 192.168.10.100.
If all of the above steps are complete you should be greeted with welcome page from nginx.


To exit the VM run `exit`
The VM can also be removed by running `vagrant destroy` but to stop the VM run `vagrant suspend`
