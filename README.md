# Vagrant Project : 

[![spotify-github-profile](https://spotify-github-profile.vercel.app/api/view?uid=1148941328&cover_image=true&theme=default&show_offline=false&background_color=121212&interchange=false&bar_color_cover=true)](https://spotify-github-profile.vercel.app/api/view?uid=1148941328&redirect=true)

BOX : generic/rhel8 [4.2.14](https://app.vagrantup.com/boxes/search)

PROVIDERS : 
* virtualbox
* vmware
* custom

Vagrant Synced Folders used to share Ansible playbooks provisioned via 'ansible_local'

# Environment
* Windows 10 Home Edition 
* Windows Services for Linux 2 [1.1.3.0](https://learn.microsoft.com/en-us/windows/wsl/install)
  * Oracle Linux 8.5
  
  
  ``$echo "alias 'vagrant=/mnt/c/HashiCorp/Vagrant/bin/vagrant.exe'" >> ~/.bashrc``
* Vagrant [Windows AMD64 2.3.4](https://releases.hashicorp.com/vagrant/2.3.4/vagrant_2.3.4_windows_amd64.msi)
* Vagrant VMware Utility [Binary Download for Windows X86_64 1.0.21](https://releases.hashicorp.com/vagrant-vmware-utility/1.0.21/vagrant-vmware-utility_1.0.21_x86_64.msi)
* VMware Workstation 16 Player [16.2.5](https://docs.vmware.com/en/VMware-Workstation-Player-for-Windows/16.0/com.vmware.player.win.using.doc/GUID-B8509247-258C-4B11-8637-5DABACEA4965.html)
* Oracle VM VirtualBox Manager [7.0.6](https://www.virtualbox.org/manual/ch01.html#intro-installing)

# Tools
``$getips <provider>``
  
``$getprivkeys <provider>``

Harvest the private keys and sow them converted ready for use by PuTTY which is much more conventient/speedy than using ``vagrant ssh``

# Links
Accidentally included secrets in your source code? 
* [git-filter-repo](https://github.com/newren/git-filter-repo)

# RHN Secrets
``$cat .secrets.rb``

![image](https://user-images.githubusercontent.com/14337141/226586884-51f173bd-2807-4c40-8d96-d1181dc58b91.png)

# Vagrant Add Box

``$python3 -m http.server 8000 &``

Add the BOX locally

``$cd /mnt/d/Virtual_Machines/GOLD`` 

``$vagrant box add --name pauliopolis/rhel8 gold-virtualbox-rhel8.box``

This method won't allow you to specify a version so use a metadata.json instead

``$vagrant box add metadata-file.json``

or


``$python3 -m http.server 8000 &``

``$vagrant box add metadata-http.json``


Alternatively - upload the BOX to [Vagrant Cloud](https://app.vagrantup.com/boxes/search)


``$vagrant box add pauliopolis/rhel8``

# Vagrant Usage

``cd vagrant/custom``
virtualbox & vmware project Vagrantfiles differ and remain works in progress currently

``$vagrant up``

``$vagrant provision --provision-with update,certs,vga``

``$vagrant reload`` In order to boot with the previously updated kernel & VBox Guest Additions

# Examples

``$vagrant up``

![image](https://user-images.githubusercontent.com/14337141/232779138-884808cf-692e-41a7-86f6-2ea9e9048040.png)
