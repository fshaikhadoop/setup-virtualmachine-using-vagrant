# setup-virtualmachine-using-vagrant
steps to create centos 7 virtual machine using vagrant 

#########################Prerequisites##########################

--- any base OS -(Linux , windows, ubuntu etc)----Here am using CentOS 7
--- any virtualization software to be installed priorly -( libvirt(kvm) , Virtualbox, VMware )
--- vagrant must be instaled and configured correctly. here am using Vagrant Installed Version: 2.1.2
--- use any user with sudo permissions to do the task.


###########setting up centos7 Vitualmachine using Vagrant#############
After the completion of vagrant intalltion now we can proceed with setup of centos7 vm.

--> first create a vagrant folder for VM in ur base machine.
    $mkdir /data/centos7 
--> Download Centos7 or <the box u need> Vagrant box from the below url 
        http://cloud.centos.org/centos/7/vagrant/x86_64/images/
  there are lots of boxes available ready in the above url, u can search based on ur requirement and download it.
   --->>> for centos7 i have selected v1905.1

--> from the above url u have to choose appropriate box based on the type of virtalaization software we use and type of OS u want 32-bit or 64-bit.
-

->as I am using basic libvirt-- I have selected 
       http://cloud.centos.org/centos/7/vagrant/x86_64/images/CentOS-7-x86_64-Vagrant-1905_01.Libvirt.box
  --->>>u can select based on the virtualization softwware u r using.


--> Once the download completes, copy the .box file the created vagrant folder or u can download the .box file directly into that folder.   
   $mv /home/user/Downloads/****.box /data/centos7/
-

-> Now open the terminal and go to the folder of the vagrant box.
   $cd /data/centos7


Now add the box to vagrant by using below command
   $vagrant box add <boxname>.box --name centos7  ### --name tag is used to recognize the vagrnat box easily. u can replace name centos7 with any name u want.


-->once it is successfully add u will get the message " the box is successfully added to libvirt " <<if u r using virualbox then u will see the message as " the box is successfully added to vitualbox " 


-->Now we have to initialize the vagrant box by using 
  $vagrant init
  once the initiaization is done, corresponding "Vagrantfile" will be created in the directory.
-->   
  
