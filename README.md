# Vagrant Project : 

BOX : generic/rhel8 (4.2.14)

PROVIDERS : 
* virtualbox
* vmware_desktop

Vagrant Synced Folders used to share Ansible playbooks provisioned via 'ansible_local'

# Environment
* Windows 10 Home Edition 
* Windows Services for Linux 2 (1.1.3.0)
  * Oracle Linux 8.5
  
  
  ``$echo "alias 'vagrant=/mnt/c/HashiCorp/Vagrant/bin/vagrant.exe'" >> ~/.bashrc``
* Vagrant (Windows AMD64 2.3.4)    
  [Windows AMD64 2.3.4](https://releases.hashicorp.com/vagrant/2.3.4/vagrant_2.3.4_windows_amd64.msi)
* Vagrant VMware Utility (Binary Download for Windows X86_64 1.0.21)
* VMware Workstation 16 Player (16.2.5)
* Oracle VM VirtualBox Manager (7.0.6)

# Tools
``$getips <provider>``
  
``$getprivkeys <provider>``
Harvest the private keys and sow them converted ready for use by PuTTY which is much more conventient/speedy than using ``vagrant ssh``

# Links
Accidentally included secrets in your source code? 
* https://github.com/newren/git-filter-repo

# RHN Secrets
``$cat .secrets.rb``

![image](https://user-images.githubusercontent.com/14337141/226586884-51f173bd-2807-4c40-8d96-d1181dc58b91.png)
