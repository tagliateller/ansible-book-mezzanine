# Ansible Up and Running

```console
azure group create linux-test-group "East US"
```

```console
azure vm quick-create linux-test-group linux-single-machine "East US" linux OpenLogic:CentOS:7.1:7.1.20150731 azureuser PASSWORD
```

info:    Executing command vm quick-create
+ Looking up the VM "linux-single-machine"                                     
info:    Using the VM Size "Standard_D1"
info:    The [OS, Data] Disk or image configuration requires storage account
+ Retrieving storage accounts                                                  
info:    Could not find any storage accounts in the region "eastus", trying to create new one
+ Creating storage account "cli99e65f0e5fdb45cb14489" in "eastus"              
+ Looking up the storage account cli99e65f0e5fdb45cb14489                      
+ Looking up the NIC "linux-eastu-1448993139446-nic"                           
info:    An nic with given name "linux-eastu-1448993139446-nic" not found, creating a new one
+ Looking up the virtual network "linux-eastu-1448993139446-vnet"              
info:    Preparing to create new virtual network and subnet
/ Creating a new virtual network "linux-eastu-1448993139446-vnet" [address prefix: "10.0.0.0/16"] with subnet "linux-eastu-1448993139446-snet" [address prefix+ "10.0.1.0/24"]
+ Looking up the virtual network "linux-eastu-1448993139446-vnet"              
+ Looking up the subnet "linux-eastu-1448993139446-snet" under the virtual network "linux-eastu-1448993139446-vnet"
info:    Found public ip parameters, trying to setup PublicIP profile
+ Looking up the public ip "linux-eastu-1448993139446-pip"                     
info:    PublicIP with given name "linux-eastu-1448993139446-pip" not found, creating a new one
+ Creating public ip "linux-eastu-1448993139446-pip"                           
+ Looking up the public ip "linux-eastu-1448993139446-pip"                     
+ Creating NIC "linux-eastu-1448993139446-nic"                                 
+ Looking up the NIC "linux-eastu-1448993139446-nic"                           
+ Creating VM "linux-single-machine"                                           
+ Looking up the VM "linux-single-machine"                                     
+ Looking up the NIC "linux-eastu-1448993139446-nic"                           
+ Looking up the public ip "linux-eastu-1448993139446-pip"                     
data:    Id                              :/subscriptions/f9ba1f95-5564-4aca-a2fd-d15b6f0175f9/resourceGroups/linux-test-group/providers/Microsoft.Compute/virtualMachines/linux-single-machine
data:    ProvisioningState               :Succeeded
data:    Name                            :linux-single-machine
data:    Location                        :eastus
data:    FQDN                            :linux-eastu-1448993139446-pip.eastus.cloudapp.azure.com
data:    Type                            :Microsoft.Compute/virtualMachines
data:    
data:    Hardware Profile:
data:      Size                          :Standard_D1
data:    
data:    Storage Profile:
data:      Image reference:
data:        Publisher                   :OpenLogic
data:        Offer                       :CentOS
data:        Sku                         :7.1
data:        Version                     :7.1.20150731
data:    
data:      OS Disk:
data:        OSType                      :Linux
data:        Name                        :cli99e65f0e5fdb45cb-os-1448993139861
data:        Caching                     :ReadWrite
data:        CreateOption                :FromImage
data:        Vhd:
data:          Uri                       :https://cli99e65f0e5fdb45cb14489.blob.core.windows.net/vhds/cli99e65f0e5fdb45cb-os-1448993139861.vhd
data:    
data:    OS Profile:
data:      Computer Name                 :linux-single-machine
data:      User Name                     :azureuser
data:      Linux Configuration:
data:        Disable Password Auth       :false
data:    
data:    Network Profile:
data:      Network Interfaces:
data:        Network Interface #1:
data:          Id                        :/subscriptions/f9ba1f95-5564-4aca-a2fd-d15b6f0175f9/resourceGroups/linux-test-group/providers/Microsoft.Network/networkInterfaces/linux-eastu-1448993139446-nic
data:          Primary                   :true
data:          MAC Address               :00-0D-3A-10-0D-BD
data:          Provisioning State        :Succeeded
data:          Name                      :linux-eastu-1448993139446-nic
data:          Location                  :eastus
data:            Private IP alloc-method :Dynamic
data:            Private IP address      :10.0.1.4
data:            Public IP address       :40.117.47.87
data:            FQDN                    :linux-eastu-1448993139446-pip.eastus.cloudapp.azure.com
data:    
data:    Diagnostics Profile:
data:    
data:      Diagnostics Instance View:
info:    vm quick-create command OK
[ec2-user@ip-172-31-11-251 ansible-book-mezzanine]$ 

TODO: ssh-key einbringen

# Löschen der Maschine

```console
azure group delete linux-test-group
```

[ec2-user@ip-172-31-11-251 ansible-book-mezzanine]$ azure group delete linux-test-group
info:    Executing command group delete
Delete resource group linux-test-group? [y/n] y
+ Deleting resource group linux-test-group                                     
info:    group delete command OK
[ec2-user@ip-172-31-11-251 ansible-book-mezzanine]$ 

# Anlegen der Maschine im ARM - Mode mit SSH-Key

```console
[ec2-user@ip-172-31-53-132 ~]$ azure vm create --nic-name testnic --public-ip-name testpip --image-urn OpenLogic:CentOS:7.1:7.1.20150731 --admin-username azure
user --ssh-publickey-file ~/azure-key-pair.pub --location eastus --vnet-name testvnet --vnet-subnet-name testsubnet testgrp testvm linux
info:    Executing command vm create
+ Looking up the VM "testvm"
info:    Verifying the public key SSH file: /home/ec2-user/azure-key-pair.pub
info:    Using the VM Size "Standard_A1"
info:    The [OS, Data] Disk or image configuration requires storage account
+ Retrieving storage accounts
info:    Using the storage account "clidd0bed2344be0eee14491" in "eastus"
+ Looking up the NIC "testnic"
info:    An nic with given name "testnic" not found, creating a new one
+ Looking up the virtual network "testvnet"
info:    Found an existing virtual network "testvnet"
info:    Existing Subnets:
info:      testsubnet:10.0.0.0/27
info:    Verifying subnet
+ Looking up the subnet "testsubnet" under the virtual network "testvnet"
info:    Subnet with given name "testsubnet" exists under the virtual network "testvnet", using this subnet
info:    Found public ip parameters, trying to setup PublicIP profile
+ Looking up the public ip "testpip"
info:    PublicIP with given name "testpip" not found, creating a new one
Enter public IP domain name: demov3-master
+ Creating public ip "testpip"
+ Looking up the public ip "testpip"
+ Creating NIC "testnic"
+ Looking up the NIC "testnic"
+ Creating VM "testvm"
info:    vm create command OK
[ec2-user@ip-172-31-53-132 ~]$
```
Hier fehlt noch der Parameter --public-ip-domain-name

# Noch ein Versuch 
```console
azure config mode arm
azure group create testgrp
azure vm create --nic-name testnic --public-ip-name testpip --image-urn OpenLogic:CentOS:7.1:7.1.20150731 --admin-username azureuser --ssh-publickey-file ~/azure-key-pair.pub --location eastus --vnet-name testvnet --vnet-subnet-name testsubnet --public-ip-domain-name demov3-master testgrp testvm linux
```
