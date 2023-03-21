# Vagrant Project : 

BOX : generic/rhel8 (4.2.14)

PROVIDERS : 
* virtualbox
* vmware_desktop

Vagrant Synced Folders used to share Ansible playbooks provisioned via 'ansible_local'

# Tools
``$getips <provider>``
  
``$getprivkeys <provider>``
Harvest the private keys and sow them converted ready for use by PuTTY which is much more conventient/speedy than using ``vagrant ssh``

# Links
Accidentally included secrets in your source code? 
* https://github.com/newren/git-filter-repo

# Secrets
Your RHN secrets ``./vagrant/virtualbox/.secrets.rb``

``module Secrets
        RHUSER = "<username>"
        RHPASS = "<password>"
end``
