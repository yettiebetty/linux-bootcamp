# Lab 2: Manage Linux VMs with the Azure CLI

1. Create resource group
2. Create virtual machine
3. Connect to VM
4. Understand VM images
5. Understand VM sizes
6. VM power states
7. Management tasks

### Notes:

Quickstart: Create a Linux VM
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-vm

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart

# Notes     @yettiebetty
1. Created resource group
2. Created virtual machine
3. Connected to VM (webserver)
4. Read to understand VM images
5. Read to understand VM sizes
6. Ran commands (Stop and start to view the different power states of the VM (webserver) power states
7. Did some Management tasks to practice

DONE!

# copy of azure bash shell commands i ran.
Requesting a Cloud Shell.Succeeded.
Connecting terminal...

yetunde@Azure:~$ az vm create \
>     --resource-group ytarg \
>     --name webserverlab2\
>     --image UbuntuLTS \
>     --admin-username akinboyt \
>    az ssh vm --ip 40.88.124.12 --akinboyt_key.pem key --akinboyt@40.88.124.12 key.pub
unrecognized arguments: az ssh vm --ip 40.88.124.12 --akinboyt_key.pem key --akinboyt@40.88.124.12 key.pub

Examples from AI knowledge base:
az vm create --name MyVm --resource-group MyResourceGroup --image RedHat:RHEL:7-RAW:7.4.2018010506
Create a default RedHat VM with automatic SSH authentication using an image URN.

az vm create --name MyVm --resource-group rg1 --image debian --assign-identity /subscriptions/99999999-1bf0-4dda-aec3-cb9272f09590/resourcegroups/myRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/myID
Create a debian VM with a user assigned identity.

az vm list
List all VMs.

https://docs.microsoft.com/en-US/cli/azure/vm#az_vm_create
Read more about the command in reference docs
yetunde@Azure:~$ az vm create \
>     --resource-group ytarg \
>     --name webserverlab2\
>     --image UbuntuLTS \
>     --admin-username akinboyt \
>    az ssh vm --ip 40.88.124.12 --private-key-file akinboyt_key.pem  --akinboyt@40.88.124.12 key.pub
unrecognized arguments: az ssh vm --ip 40.88.124.12 --private-key-file akinboyt_key.pem --akinboyt@40.88.124.12 key.pub

Examples from AI knowledge base:
az vm create --name MyVm --resource-group MyResourceGroup --image RedHat:RHEL:7-RAW:7.4.2018010506
Create a default RedHat VM with automatic SSH authentication using an image URN.

az vm create --name MyVm --resource-group rg1 --image debian --assign-identity /subscriptions/99999999-1bf0-4dda-aec3-cb9272f09590/resourcegroups/myRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/myID
Create a debian VM with a user assigned identity.

az vm list
List all VMs.

https://docs.microsoft.com/en-US/cli/azure/vm#az_vm_create
Read more about the command in reference docsyetunde@Azure:~$ az vm create     --resource-group ytarg     --name webserverlab2    --image UbuntuLTS     --admin-username akinboytAn RSA key file or key value must be supplied to SSH Key Value. You can use --generate-ssh-keys to let CLI generate one for you
yetunde@Azure:~$ lsclouddrive
yetunde@Azure:~$ az vm create     --resource-group ytarg     --name webserverlab2    --image UbuntuLTS     --admin-username akinboyt  --ip 40.88.124.12 --private-key-file akinboyt_key.pem  --akinboyt@40.88.124.12 key.pub
unrecognized arguments: --ip 40.88.124.12 --private-key-file akinboyt_key.pem --akinboyt@40.88.124.12 key.pub

Examples from AI knowledge base:
az vm create --name MyVm --resource-group MyResourceGroup --image RedHat:RHEL:7-RAW:7.4.2018010506
Create a default RedHat VM with automatic SSH authentication using an image URN.

az vm create --name MyVm --resource-group rg1 --image debian --assign-identity /subscriptions/99999999-1bf0-4dda-aec3-cb9272f09590/resourcegroups/myRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/myID
Create a debian VM with a user assigned identity.

az vm list
List all VMs.

https://docs.microsoft.com/en-US/cli/azure/vm#az_vm_create
Read more about the command in reference docs
yetunde@Azure:~$ az vm create     --resource-group ytarg     --name webserverlab2    --image UbuntuLTS     --admin-username akinboyt    ssh vm --ip 40.88.124.12 --private-key-file akinboyt_key.pem  --akinboyt@40.88.124.12 key.pub
unrecognized arguments: ssh vm --ip 40.88.124.12 --private-key-file akinboyt_key.pem --akinboyt@40.88.124.12 key.pub

Examples from AI knowledge base:
az vm create --name MyVm --resource-group MyResourceGroup --image RedHat:RHEL:7-RAW:7.4.2018010506
Create a default RedHat VM with automatic SSH authentication using an image URN.

az vm create --name MyVm --resource-group rg1 --image debian --assign-identity /subscriptions/99999999-1bf0-4dda-aec3-cb9272f09590/resourcegroups/myRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/myID
Create a debian VM with a user assigned identity.

az vm list
List all VMs.

https://docs.microsoft.com/en-US/cli/azure/vm#az_vm_create
Read more about the command in reference docs
yetunde@Azure:~$ az vm create     --resource-group ytarg     --name webserverlab2    --image UbuntuLTS     --admin-username akinboyt     --ssh vm --ip 40.88.124.12 --private-key-file akinboyt_key.pem  --akinboyt@40.88.124.12 key.pub
ambiguous option: --ssh could match --ssh-dest-key-path, --ssh-key-values, --ssh-key-name

Examples from AI knowledge base:
az vm create --name MyVm --resource-group MyResourceGroup --image RedHat:RHEL:7-RAW:7.4.2018010506
Create a default RedHat VM with automatic SSH authentication using an image URN.

az vm image list
List the VM/VMSS images available in the Azure Marketplace. (autogenerated)

az group create --location westus --resource-group MyResourceGroup
Create a new resource group in the West US region.

https://docs.microsoft.com/en-US/cli/azure/vm#az_vm_create
Read more about the command in reference docs
yetunde@Azure:~$ az vm create     --resource-group ytarg     --name webserverlab2    --image UbuntuLTS     --admin-username akinboyt  ;An RSA key file or key value must be supplied to SSH Key Value. You can use --generate-ssh-keys to let CLI generate one for you
yetunde@Azure:~$ az vm create     --resource-group ytarg     --name webserverlab2    --image UbuntuLTS     --admin-username akinboyt  --generate-ssh-keys
SSH key files '/home/yetunde/.ssh/id_rsa' and '/home/yetunde/.ssh/id_rsa.pub' have been generated under ~/.ssh to allow SSH access to the VM. If using machines without permanent storage, back up your keys to a safe location.
It is recommended to use parameter "--public-ip-sku Standard" to create new VM with Standard public IP. Please note that the default public IP used for VM creation will be changed from Basic to Standardin the future.
{
  "fqdns": "",
  "id": "/subscriptions/ebd0efd8-e011-4639-8831-641041145f77/resourceGroups/ytarg/providers/Microsoft.Compute/virtualMachines/webserverlab2",
  "location": "westeurope",
  "macAddress": "60-45-BD-87-72-C4",
  "powerState": "VM running",
  "privateIpAddress": "10.0.0.4",
  "publicIpAddress": "20.71.172.18",
  "resourceGroup": "ytarg",
  "zones": ""
}
yetunde@Azure:~$ ssh akinboyt@20.71.172.18
The authenticity of host '20.71.172.18 (20.71.172.18)' can't be established.
ECDSA key fingerprint is SHA256:kpvUhWAcChmbvoNy8lJuUhEci8UjI4ehdzivvhWNrbg.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '20.71.172.18' (ECDSA) to the list of known hosts.
Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 5.4.0-1063-azure x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Fri Nov 19 13:41:41 UTC 2021

  System load:  0.0               Processes:           108
  Usage of /:   4.6% of 28.90GB   Users logged in:     0
  Memory usage: 5%                IP address for eth0: 10.0.0.4
  Swap usage:   0%

0 updates can be applied immediately.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

akinboyt@webserverlab2:~$ az vm image list --output table
az: command not found
akinboyt@webserverlab2:~$ exit
logout
Connection to 20.71.172.18 closed.
yetunde@Azure:~$ az vm show --resource-group ytarg --name webserver --query hardwareProfile.vmSize
"Standard_B1s"
yetunde@Azure:~$ az vm list-vm-resize-options --resource-group myResourceGroupVM --name myVM --query [Standard_DS4_v2].name
yetunde@Azure:~$ az vm list-vm-resize-options --resource-group myResourceGroupVM --name myVM --query [Standard_DS4_v2].name
yetunde@Azure:~$ az vm list-vm-resize-options --resource-group ytarg --name webserver --query [Standard_DS4_v2].name
yetunde@Azure:~$ az vm deallocate --resource-group ytarg --name webserver
yetunde@Azure:~$ az vm list-vm-resize-options --resource-group ytarg --name webserver --query [Standard_DS4_v2].name
yetunde@Azure:~$ az vm resize --resource-group ytarg --name webserver --size Standard_DS4_.name
(InvalidParameter) The value Standard_DS4_.name provided for the VM size is not valid. The valid sizes in the current region are: Standard_B1ls,Standard_B1ms,Standard_B1s,Standard_B2ms,Standard_B2s,Standard_B4ms,Standard_B8ms,Standard_B12ms,Standard_B16ms,Standard_B20ms,Standard_DS1_v2,Standard_DS2_v2,Standard_DS3_v2,Standard_DS4_v2,Standard_DS5_v2,Standard_DS11-1_v2,Standard_DS11_v2,Standard_DS12-1_v2,Standard_DS12-2_v2,Standard_DS12_v2,Standard_DS13-2_v2,Standard_DS13-4_v2,Standard_DS13_v2,Standard_DS14-4_v2,Standard_DS14-8_v2,Standard_DS14_v2,Standard_DS15_v2,Standard_DS2_v2_Promo,Standard_DS3_v2_Promo,Standard_DS4_v2_Promo,Standard_DS5_v2_Promo,Standard_DS11_v2_Promo,Standard_DS12_v2_Promo,Standard_DS13_v2_Promo,Standard_DS14_v2_Promo,Standard_F1s,Standard_F2s,Standard_F4s,Standard_F8s,Standard_F16s,Standard_D2s_v3,Standard_D4s_v3,Standard_D8s_v3,Standard_D16s_v3,Standard_D32s_v3,Standard_D2a_v4,Standard_D4a_v4,Standard_D8a_v4,Standard_D16a_v4,Standard_D32a_v4,Standard_D48a_v4,Standard_D64a_v4,Standard_D96a_v4,Standard_D2as_v4,Standard_D4as_v4,Standard_D8as_v4,Standard_D16as_v4,Standard_D32as_v4,Standard_D48as_v4,Standard_D64as_v4,Standard_D96as_v4,Standard_E2a_v4,Standard_E4a_v4,Standard_E8a_v4,Standard_E16a_v4,Standard_E20a_v4,Standard_E32a_v4,Standard_E48a_v4,Standard_E64a_v4,Standard_E96a_v4,Standard_E2as_v4,Standard_E4-2as_v4,Standard_E4as_v4,Standard_E8-2as_v4,Standard_E8-4as_v4,Standard_E8as_v4,Standard_E16-4as_v4,Standard_E16-8as_v4,Standard_E16as_v4,Standard_E20as_v4,Standard_E32-8as_v4,Standard_E32-16as_v4,Standard_E32as_v4,Standard_E48as_v4,Standard_E64-16as_v4,Standard_E64-32as_v4,Standard_E64as_v4,Standard_E96-24as_v4,Standard_E96-48as_v4,Standard_E96as_v4,Standard_D1_v2,Standard_D2_v2,Standard_D3_v2,Standard_D4_v2,Standard_D5_v2,Standard_D11_v2,Standard_D12_v2,Standard_D13_v2,Standard_D14_v2,Standard_D15_v2,Standard_D2_v2_Promo,Standard_D3_v2_Promo,Standard_D4_v2_Promo,Standard_D5_v2_Promo,Standard_D11_v2_Promo,Standard_D12_v2_Promo,Standard_D13_v2_Promo,Standard_D14_v2_Promo,Standard_F1,Standard_F2,Standard_F4,Standard_F8,Standard_F16,Standard_A1_v2,Standard_A2m_v2,Standard_A2_v2,Standard_A4m_v2,Standard_A4_v2,Standard_A8m_v2,Standard_A8_v2,Standard_D2_v3,Standard_D4_v3,Standard_D8_v3,Standard_D16_v3,Standard_D32_v3,Standard_D48_v3,Standard_D64_v3,Standard_D48s_v3,Standard_D64s_v3,Standard_E2_v3,Standard_E4_v3,Standard_E8_v3,Standard_E16_v3,Standard_E20_v3,Standard_E32_v3,Standard_E48_v3,Standard_E64_v3,Standard_E2s_v3,Standard_E4-2s_v3,Standard_E4s_v3,Standard_E8-2s_v3,Standard_E8-4s_v3,Standard_E8s_v3,Standard_E16-4s_v3,Standard_E16-8s_v3,Standard_E16s_v3,Standard_E20s_v3,Standard_E32-8s_v3,Standard_E32-16s_v3,Standard_E32s_v3,Standard_E48s_v3,Standard_E64-16s_v3,Standard_E64-32s_v3,Standard_E64s_v3,Standard_A0,Standard_A1,Standard_A2,Standard_A3,Standard_A5,Standard_A4,Standard_A6,Standard_A7,Basic_A0,Basic_A1,Basic_A2,Basic_A3,Basic_A4,Standard_E64i_v3,Standard_E64is_v3,Standard_M208ms_v2,Standard_M208s_v2,Standard_M416-208s_v2,Standard_M416s_v2,Standard_M416-208ms_v2,Standard_M416ms_v2,Standard_H8,Standard_H8_Promo,Standard_H16,Standard_H16_Promo,Standard_H8m,Standard_H8m_Promo,Standard_H16m,Standard_H16m_Promo,Standard_H16r,Standard_H16r_Promo,Standard_H16mr,Standard_H16mr_Promo,Standard_D1,Standard_D2,Standard_D3,Standard_D4,Standard_D11,Standard_D12,Standard_D13,Standard_D14,Standard_NV6,Standard_NV12,Standard_NV24,Standard_NV6_Promo,Standard_NV12_Promo,Standard_NV24_Promo,Standard_NC4as_T4_v3,Standard_NC8as_T4_v3,Standard_NC16as_T4_v3,Standard_NC64as_T4_v3,Standard_NV6s_v2,Standard_NV12s_v2,Standard_NV24s_v2,Standard_NV12s_v3,Standard_NV24s_v3,Standard_NV48s_v3,Standard_HB120rs_v2,Standard_D2ds_v4,Standard_D4ds_v4,Standard_D8ds_v4,Standard_D16ds_v4,Standard_D32ds_v4,Standard_D48ds_v4,Standard_D64ds_v4,Standard_D2ds_v5,Standard_D4ds_v5,Standard_D8ds_v5,Standard_D16ds_v5,Standard_D32ds_v5,Standard_D48ds_v5,Standard_D64ds_v5,Standard_D96ds_v5,Standard_D2d_v4,Standard_D4d_v4,Standard_D8d_v4,Standard_D16d_v4,Standard_D32d_v4,Standard_D48d_v4,Standard_D64d_v4,Standard_D2d_v5,Standard_D4d_v5,Standard_D8d_v5,Standard_D16d_v5,Standard_D32d_v5,Standard_D48d_v5,Standard_D64d_v5,Standard_D96d_v5,Standard_D2s_v4,Standard_D4s_v4,Standard_D8s_v4,Standard_D16s_v4,Standard_D32s_v4,Standard_D48s_v4,Standard_D64s_v4,Standard_D2s_v5,Standard_D4s_v5,Standard_D8s_v5,Standard_D16s_v5,Standard_D32s_v5,Standard_D48s_v5,Standard_D64s_v5,Standard_D96s_v5,Standard_D2_v4,Standard_D4_v4,Standard_D8_v4,Standard_D16_v4,Standard_D32_v4,Standard_D48_v4,Standard_D64_v4,Standard_D2_v5,Standard_D4_v5,Standard_D8_v5,Standard_D16_v5,Standard_D32_v5,Standard_D48_v5,Standard_D64_v5,Standard_D96_v5,Standard_E2ds_v4,Standard_E4-2ds_v4,Standard_E4ds_v4,Standard_E8-2ds_v4,Standard_E8-4ds_v4,Standard_E8ds_v4,Standard_E16-4ds_v4,Standard_E16-8ds_v4,Standard_E16ds_v4,Standard_E20ds_v4,Standard_E32-8ds_v4,Standard_E32-16ds_v4,Standard_E32ds_v4,Standard_E48ds_v4,Standard_E64-16ds_v4,Standard_E64-32ds_v4,Standard_E64ds_v4,Standard_E80ids_v4,Standard_E2ds_v5,Standard_E4-2ds_v5,Standard_E4ds_v5,Standard_E8-2ds_v5,Standard_E8-4ds_v5,Standard_E8ds_v5,Standard_E16-4ds_v5,Standard_E16-8ds_v5,Standard_E16ds_v5,Standard_E20ds_v5,Standard_E32-8ds_v5,Standard_E32-16ds_v5,Standard_E32ds_v5,Standard_E48ds_v5,Standard_E64-16ds_v5,Standard_E64-32ds_v5,Standard_E64ds_v5,Standard_E96-24ds_v5,Standard_E96-48ds_v5,Standard_E96ds_v5,Standard_E104ids_v5,Standard_E2d_v4,Standard_E4d_v4,Standard_E8d_v4,Standard_E16d_v4,Standard_E20d_v4,Standard_E32d_v4,Standard_E48d_v4,Standard_E64d_v4,Standard_E2d_v5,Standard_E4d_v5,Standard_E8d_v5,Standard_E16d_v5,Standard_E20d_v5,Standard_E32d_v5,Standard_E48d_v5,Standard_E64d_v5,Standard_E96d_v5,Standard_E104id_v5,Standard_E2s_v4,Standard_E4-2s_v4,Standard_E4s_v4,Standard_E8-2s_v4,Standard_E8-4s_v4,Standard_E8s_v4,Standard_E16-4s_v4,Standard_E16-8s_v4,Standard_E16s_v4,Standard_E20s_v4,Standard_E32-8s_v4,Standard_E32-16s_v4,Standard_E32s_v4,Standard_E48s_v4,Standard_E64-16s_v4,Standard_E64-32s_v4,Standard_E64s_v4,Standard_E80is_v4,Standard_E2s_v5,Standard_E4-2s_v5,Standard_E4s_v5,Standard_E8-2s_v5,Standard_E8-4s_v5,Standard_E8s_v5,Standard_E16-4s_v5,Standard_E16-8s_v5,Standard_E16s_v5,Standard_E20s_v5,Standard_E32-8s_v5,Standard_E32-16s_v5,Standard_E32s_v5,Standard_E48s_v5,Standard_E64-16s_v5,Standard_E64-32s_v5,Standard_E64s_v5,Standard_E96-24s_v5,Standard_E96-48s_v5,Standard_E96s_v5,Standard_E104is_v5,Standard_E2_v4,Standard_E4_v4,Standard_E8_v4,Standard_E16_v4,Standard_E20_v4,Standard_E32_v4,Standard_E48_v4,Standard_E64_v4,Standard_E2_v5,Standard_E4_v5,Standard_E8_v5,Standard_E16_v5,Standard_E20_v5,Standard_E32_v5,Standard_E48_v5,Standard_E64_v5,Standard_E96_v5,Standard_E104i_v5,Standard_F2s_v2,Standard_F4s_v2,Standard_F8s_v2,Standard_F16s_v2,Standard_F32s_v2,Standard_F48s_v2,Standard_F64s_v2,Standard_F72s_v2,Standard_NC6s_v2,Standard_NC12s_v2,Standard_NC24rs_v2,Standard_NC24s_v2,Standard_NC6,Standard_NC12,Standard_NC24,Standard_NC24r,Standard_NC6_Promo,Standard_NC12_Promo,Standard_NC24_Promo,Standard_NC24r_Promo,Standard_DS1,Standard_DS2,Standard_DS3,Standard_DS4,Standard_DS11,Standard_DS12,Standard_DS13,Standard_DS14,Standard_L8s_v2,Standard_L16s_v2,Standard_L32s_v2,Standard_L48s_v2,Standard_L64s_v2,Standard_L80s_v2,Standard_M64,Standard_M64m,Standard_M128,Standard_M128m,Standard_M8-2ms,Standard_M8-4ms,Standard_M8ms,Standard_M16-4ms,Standard_M16-8ms,Standard_M16ms,Standard_M32-8ms,Standard_M32-16ms,Standard_M32ls,Standard_M32ms,Standard_M32ts,Standard_M64-16ms,Standard_M64-32ms,Standard_M64ls,Standard_M64ms,Standard_M64s,Standard_M128-32ms,Standard_M128-64ms,Standard_M128ms,Standard_M128s,Standard_M32ms_v2,Standard_M64ms_v2,Standard_M64s_v2,Standard_M128ms_v2,Standard_M128s_v2,Standard_M192ims_v2,Standard_M192is_v2,Standard_M32dms_v2,Standard_M64dms_v2,Standard_M64ds_v2,Standard_M128dms_v2,Standard_M128ds_v2,Standard_M192idms_v2,Standard_M192ids_v2,Standard_DC8_v2,Standard_DC1s_v2,Standard_DC2s_v2,Standard_DC4s_v2,Standard_ND40rs_v2,Standard_FX4mds,Standard_FX12mds,Standard_FX24mds,Standard_FX36mds,Standard_FX48mds,Standard_NP10s,Standard_NP20s,Standard_NP40s,Standard_D2as_v5,Standard_D4as_v5,Standard_D8as_v5,Standard_D16as_v5,Standard_D32as_v5,Standard_D48as_v5,Standard_D64as_v5,Standard_D96as_v5,Standard_E2as_v5,Standard_E4-2as_v5,Standard_E4as_v5,Standard_E8-2as_v5,Standard_E8-4as_v5,Standard_E8as_v5,Standard_E16-4as_v5,Standard_E16-8as_v5,Standard_E16as_v5,Standard_E20as_v5,Standard_E32-8as_v5,Standard_E32-16as_v5,Standard_E32as_v5,Standard_E48as_v5,Standard_E64-16as_v5,Standard_E64-32as_v5,Standard_E64as_v5,Standard_E96-24as_v5,Standard_E96-48as_v5,Standard_E96as_v5,Standard_D2ads_v5,Standard_D4ads_v5,Standard_D8ads_v5,Standard_D16ads_v5,Standard_D32ads_v5,Standard_D48ads_v5,Standard_D64ads_v5,Standard_D96ads_v5,Standard_E2ads_v5,Standard_E4-2ads_v5,Standard_E4ads_v5,Standard_E8-2ads_v5,Standard_E8-4ads_v5,Standard_E8ads_v5,Standard_E16-4ads_v5,Standard_E16-8ads_v5,Standard_E16ads_v5,Standard_E20ads_v5,Standard_E32-8ads_v5,Standard_E32-16ads_v5,Standard_E32ads_v5,Standard_E48ads_v5,Standard_E64-16ads_v5,Standard_E64-32ads_v5,Standard_E64ads_v5,Standard_E96-24ads_v5,Standard_E96-48ads_v5,Standard_E96ads_v5,Standard_HC44rs,Standard_ND6s,Standard_ND12s,Standard_ND24rs,Standard_ND24s,Standard_DC2s,Standard_DC4s,Standard_HB120-16rs_v3,Standard_HB120-32rs_v3,Standard_HB120-64rs_v3,Standard_HB120-96rs_v3,Standard_HB120rs_v3,Standard_NV4as_v4,Standard_NV8as_v4,Standard_NV16as_v4,Standard_NV32as_v4,Standard_NC6s_v3,Standard_NC12s_v3,Standard_NC24rs_v3,Standard_NC24s_v3,Standard_PB6s,Standard_HB60rs,Standard_ND96asr_v4,Standard_ND40s_v3. Find out more on the valid VM sizes in each region at https://aka.ms/azure-regions.
Code: InvalidParameter
Message: The value Standard_DS4_.name provided for the VM size is not valid. The valid sizes in the current region are: Standard_B1ls,Standard_B1ms,Standard_B1s,Standard_B2ms,Standard_B2s,Standard_B4ms,Standard_B8ms,Standard_B12ms,Standard_B16ms,Standard_B20ms,Standard_DS1_v2,Standard_DS2_v2,Standard_DS3_v2,Standard_DS4_v2,Standard_DS5_v2,Standard_DS11-1_v2,Standard_DS11_v2,Standard_DS12-1_v2,Standard_DS12-2_v2,Standard_DS12_v2,Standard_DS13-2_v2,Standard_DS13-4_v2,Standard_DS13_v2,Standard_DS14-4_v2,Standard_DS14-8_v2,Standard_DS14_v2,Standard_DS15_v2,Standard_DS2_v2_Promo,Standard_DS3_v2_Promo,Standard_DS4_v2_Promo,Standard_DS5_v2_Promo,Standard_DS11_v2_Promo,Standard_DS12_v2_Promo,Standard_DS13_v2_Promo,Standard_DS14_v2_Promo,Standard_F1s,Standard_F2s,Standard_F4s,Standard_F8s,Standard_F16s,Standard_D2s_v3,Standard_D4s_v3,Standard_D8s_v3,Standard_D16s_v3,Standard_D32s_v3,Standard_D2a_v4,Standard_D4a_v4,Standard_D8a_v4,Standard_D16a_v4,Standard_D32a_v4,Standard_D48a_v4,Standard_D64a_v4,Standard_D96a_v4,Standard_D2as_v4,Standard_D4as_v4,Standard_D8as_v4,Standard_D16as_v4,Standard_D32as_v4,Standard_D48as_v4,Standard_D64as_v4,Standard_D96as_v4,Standard_E2a_v4,Standard_E4a_v4,Standard_E8a_v4,Standard_E16a_v4,Standard_E20a_v4,Standard_E32a_v4,Standard_E48a_v4,Standard_E64a_v4,Standard_E96a_v4,Standard_E2as_v4,Standard_E4-2as_v4,Standard_E4as_v4,Standard_E8-2as_v4,Standard_E8-4as_v4,Standard_E8as_v4,Standard_E16-4as_v4,Standard_E16-8as_v4,Standard_E16as_v4,Standard_E20as_v4,Standard_E32-8as_v4,Standard_E32-16as_v4,Standard_E32as_v4,Standard_E48as_v4,Standard_E64-16as_v4,Standard_E64-32as_v4,Standard_E64as_v4,Standard_E96-24as_v4,Standard_E96-48as_v4,Standard_E96as_v4,Standard_D1_v2,Standard_D2_v2,Standard_D3_v2,Standard_D4_v2,Standard_D5_v2,Standard_D11_v2,Standard_D12_v2,Standard_D13_v2,Standard_D14_v2,Standard_D15_v2,Standard_D2_v2_Promo,Standard_D3_v2_Promo,Standard_D4_v2_Promo,Standard_D5_v2_Promo,Standard_D11_v2_Promo,Standard_D12_v2_Promo,Standard_D13_v2_Promo,Standard_D14_v2_Promo,Standard_F1,Standard_F2,Standard_F4,Standard_F8,Standard_F16,Standard_A1_v2,Standard_A2m_v2,Standard_A2_v2,Standard_A4m_v2,Standard_A4_v2,Standard_A8m_v2,Standard_A8_v2,Standard_D2_v3,Standard_D4_v3,Standard_D8_v3,Standard_D16_v3,Standard_D32_v3,Standard_D48_v3,Standard_D64_v3,Standard_D48s_v3,Standard_D64s_v3,Standard_E2_v3,Standard_E4_v3,Standard_E8_v3,Standard_E16_v3,Standard_E20_v3,Standard_E32_v3,Standard_E48_v3,Standard_E64_v3,Standard_E2s_v3,Standard_E4-2s_v3,Standard_E4s_v3,Standard_E8-2s_v3,Standard_E8-4s_v3,Standard_E8s_v3,Standard_E16-4s_v3,Standard_E16-8s_v3,Standard_E16s_v3,Standard_E20s_v3,Standard_E32-8s_v3,Standard_E32-16s_v3,Standard_E32s_v3,Standard_E48s_v3,Standard_E64-16s_v3,Standard_E64-32s_v3,Standard_E64s_v3,Standard_A0,Standard_A1,Standard_A2,Standard_A3,Standard_A5,Standard_A4,Standard_A6,Standard_A7,Basic_A0,Basic_A1,Basic_A2,Basic_A3,Basic_A4,Standard_E64i_v3,Standard_E64is_v3,Standard_M208ms_v2,Standard_M208s_v2,Standard_M416-208s_v2,Standard_M416s_v2,Standard_M416-208ms_v2,Standard_M416ms_v2,Standard_H8,Standard_H8_Promo,Standard_H16,Standard_H16_Promo,Standard_H8m,Standard_H8m_Promo,Standard_H16m,Standard_H16m_Promo,Standard_H16r,Standard_H16r_Promo,Standard_H16mr,Standard_H16mr_Promo,Standard_D1,Standard_D2,Standard_D3,Standard_D4,Standard_D11,Standard_D12,Standard_D13,Standard_D14,Standard_NV6,Standard_NV12,Standard_NV24,Standard_NV6_Promo,Standard_NV12_Promo,Standard_NV24_Promo,Standard_NC4as_T4_v3,Standard_NC8as_T4_v3,Standard_NC16as_T4_v3,Standard_NC64as_T4_v3,Standard_NV6s_v2,Standard_NV12s_v2,Standard_NV24s_v2,Standard_NV12s_v3,Standard_NV24s_v3,Standard_NV48s_v3,Standard_HB120rs_v2,Standard_D2ds_v4,Standard_D4ds_v4,Standard_D8ds_v4,Standard_D16ds_v4,Standard_D32ds_v4,Standard_D48ds_v4,Standard_D64ds_v4,Standard_D2ds_v5,Standard_D4ds_v5,Standard_D8ds_v5,Standard_D16ds_v5,Standard_D32ds_v5,Standard_D48ds_v5,Standard_D64ds_v5,Standard_D96ds_v5,Standard_D2d_v4,Standard_D4d_v4,Standard_D8d_v4,Standard_D16d_v4,Standard_D32d_v4,Standard_D48d_v4,Standard_D64d_v4,Standard_D2d_v5,Standard_D4d_v5,Standard_D8d_v5,Standard_D16d_v5,Standard_D32d_v5,Standard_D48d_v5,Standard_D64d_v5,Standard_D96d_v5,Standard_D2s_v4,Standard_D4s_v4,Standard_D8s_v4,Standard_D16s_v4,Standard_D32s_v4,Standard_D48s_v4,Standard_D64s_v4,Standard_D2s_v5,Standard_D4s_v5,Standard_D8s_v5,Standard_D16s_v5,Standard_D32s_v5,Standard_D48s_v5,Standard_D64s_v5,Standard_D96s_v5,Standard_D2_v4,Standard_D4_v4,Standard_D8_v4,Standard_D16_v4,Standard_D32_v4,Standard_D48_v4,Standard_D64_v4,Standard_D2_v5,Standard_D4_v5,Standard_D8_v5,Standard_D16_v5,Standard_D32_v5,Standard_D48_v5,Standard_D64_v5,Standard_D96_v5,Standard_E2ds_v4,Standard_E4-2ds_v4,Standard_E4ds_v4,Standard_E8-2ds_v4,Standard_E8-4ds_v4,Standard_E8ds_v4,Standard_E16-4ds_v4,Standard_E16-8ds_v4,Standard_E16ds_v4,Standard_E20ds_v4,Standard_E32-8ds_v4,Standard_E32-16ds_v4,Standard_E32ds_v4,Standard_E48ds_v4,Standard_E64-16ds_v4,Standard_E64-32ds_v4,Standard_E64ds_v4,Standard_E80ids_v4,Standard_E2ds_v5,Standard_E4-2ds_v5,Standard_E4ds_v5,Standard_E8-2ds_v5,Standard_E8-4ds_v5,Standard_E8ds_v5,Standard_E16-4ds_v5,Standard_E16-8ds_v5,Standard_E16ds_v5,Standard_E20ds_v5,Standard_E32-8ds_v5,Standard_E32-16ds_v5,Standard_E32ds_v5,Standard_E48ds_v5,Standard_E64-16ds_v5,Standard_E64-32ds_v5,Standard_E64ds_v5,Standard_E96-24ds_v5,Standard_E96-48ds_v5,Standard_E96ds_v5,Standard_E104ids_v5,Standard_E2d_v4,Standard_E4d_v4,Standard_E8d_v4,Standard_E16d_v4,Standard_E20d_v4,Standard_E32d_v4,Standard_E48d_v4,Standard_E64d_v4,Standard_E2d_v5,Standard_E4d_v5,Standard_E8d_v5,Standard_E16d_v5,Standard_E20d_v5,Standard_E32d_v5,Standard_E48d_v5,Standard_E64d_v5,Standard_E96d_v5,Standard_E104id_v5,Standard_E2s_v4,Standard_E4-2s_v4,Standard_E4s_v4,Standard_E8-2s_v4,Standard_E8-4s_v4,Standard_E8s_v4,Standard_E16-4s_v4,Standard_E16-8s_v4,Standard_E16s_v4,Standard_E20s_v4,Standard_E32-8s_v4,Standard_E32-16s_v4,Standard_E32s_v4,Standard_E48s_v4,Standard_E64-16s_v4,Standard_E64-32s_v4,Standard_E64s_v4,Standard_E80is_v4,Standard_E2s_v5,Standard_E4-2s_v5,Standard_E4s_v5,Standard_E8-2s_v5,Standard_E8-4s_v5,Standard_E8s_v5,Standard_E16-4s_v5,Standard_E16-8s_v5,Standard_E16s_v5,Standard_E20s_v5,Standard_E32-8s_v5,Standard_E32-16s_v5,Standard_E32s_v5,Standard_E48s_v5,Standard_E64-16s_v5,Standard_E64-32s_v5,Standard_E64s_v5,Standard_E96-24s_v5,Standard_E96-48s_v5,Standard_E96s_v5,Standard_E104is_v5,Standard_E2_v4,Standard_E4_v4,Standard_E8_v4,Standard_E16_v4,Standard_E20_v4,Standard_E32_v4,Standard_E48_v4,Standard_E64_v4,Standard_E2_v5,Standard_E4_v5,Standard_E8_v5,Standard_E16_v5,Standard_E20_v5,Standard_E32_v5,Standard_E48_v5,Standard_E64_v5,Standard_E96_v5,Standard_E104i_v5,Standard_F2s_v2,Standard_F4s_v2,Standard_F8s_v2,Standard_F16s_v2,Standard_F32s_v2,Standard_F48s_v2,Standard_F64s_v2,Standard_F72s_v2,Standard_NC6s_v2,Standard_NC12s_v2,Standard_NC24rs_v2,Standard_NC24s_v2,Standard_NC6,Standard_NC12,Standard_NC24,Standard_NC24r,Standard_NC6_Promo,Standard_NC12_Promo,Standard_NC24_Promo,Standard_NC24r_Promo,Standard_DS1,Standard_DS2,Standard_DS3,Standard_DS4,Standard_DS11,Standard_DS12,Standard_DS13,Standard_DS14,Standard_L8s_v2,Standard_L16s_v2,Standard_L32s_v2,Standard_L48s_v2,Standard_L64s_v2,Standard_L80s_v2,Standard_M64,Standard_M64m,Standard_M128,Standard_M128m,Standard_M8-2ms,Standard_M8-4ms,Standard_M8ms,Standard_M16-4ms,Standard_M16-8ms,Standard_M16ms,Standard_M32-8ms,Standard_M32-16ms,Standard_M32ls,Standard_M32ms,Standard_M32ts,Standard_M64-16ms,Standard_M64-32ms,Standard_M64ls,Standard_M64ms,Standard_M64s,Standard_M128-32ms,Standard_M128-64ms,Standard_M128ms,Standard_M128s,Standard_M32ms_v2,Standard_M64ms_v2,Standard_M64s_v2,Standard_M128ms_v2,Standard_M128s_v2,Standard_M192ims_v2,Standard_M192is_v2,Standard_M32dms_v2,Standard_M64dms_v2,Standard_M64ds_v2,Standard_M128dms_v2,Standard_M128ds_v2,Standard_M192idms_v2,Standard_M192ids_v2,Standard_DC8_v2,Standard_DC1s_v2,Standard_DC2s_v2,Standard_DC4s_v2,Standard_ND40rs_v2,Standard_FX4mds,Standard_FX12mds,Standard_FX24mds,Standard_FX36mds,Standard_FX48mds,Standard_NP10s,Standard_NP20s,Standard_NP40s,Standard_D2as_v5,Standard_D4as_v5,Standard_D8as_v5,Standard_D16as_v5,Standard_D32as_v5,Standard_D48as_v5,Standard_D64as_v5,Standard_D96as_v5,Standard_E2as_v5,Standard_E4-2as_v5,Standard_E4as_v5,Standard_E8-2as_v5,Standard_E8-4as_v5,Standard_E8as_v5,Standard_E16-4as_v5,Standard_E16-8as_v5,Standard_E16as_v5,Standard_E20as_v5,Standard_E32-8as_v5,Standard_E32-16as_v5,Standard_E32as_v5,Standard_E48as_v5,Standard_E64-16as_v5,Standard_E64-32as_v5,Standard_E64as_v5,Standard_E96-24as_v5,Standard_E96-48as_v5,Standard_E96as_v5,Standard_D2ads_v5,Standard_D4ads_v5,Standard_D8ads_v5,Standard_D16ads_v5,Standard_D32ads_v5,Standard_D48ads_v5,Standard_D64ads_v5,Standard_D96ads_v5,Standard_E2ads_v5,Standard_E4-2ads_v5,Standard_E4ads_v5,Standard_E8-2ads_v5,Standard_E8-4ads_v5,Standard_E8ads_v5,Standard_E16-4ads_v5,Standard_E16-8ads_v5,Standard_E16ads_v5,Standard_E20ads_v5,Standard_E32-8ads_v5,Standard_E32-16ads_v5,Standard_E32ads_v5,Standard_E48ads_v5,Standard_E64-16ads_v5,Standard_E64-32ads_v5,Standard_E64ads_v5,Standard_E96-24ads_v5,Standard_E96-48ads_v5,Standard_E96ads_v5,Standard_HC44rs,Standard_ND6s,Standard_ND12s,Standard_ND24rs,Standard_ND24s,Standard_DC2s,Standard_DC4s,Standard_HB120-16rs_v3,Standard_HB120-32rs_v3,Standard_HB120-64rs_v3,Standard_HB120-96rs_v3,Standard_HB120rs_v3,Standard_NV4as_v4,Standard_NV8as_v4,Standard_NV16as_v4,Standard_NV32as_v4,Standard_NC6s_v3,Standard_NC12s_v3,Standard_NC24rs_v3,Standard_NC24s_v3,Standard_PB6s,Standard_HB60rs,Standard_ND96asr_v4,Standard_ND40s_v3. Find out more on the valid VM sizes in each region at https://aka.ms/azure-regions.
Target: vmSize
yetunde@Azure:~$ az vm resize --resource-group ytarg --name webserver --size [Standard_DS4_v2].name
(InvalidParameter) The value [Standard_DS4_v2].name provided for the VM size is not valid. The valid sizes in the current region are: Standard_B1ls,Standard_B1ms,Standard_B1s,Standard_B2ms,Standard_B2s,Standard_B4ms,Standard_B8ms,Standard_B12ms,Standard_B16ms,Standard_B20ms,Standard_DS1_v2,Standard_DS2_v2,Standard_DS3_v2,Standard_DS4_v2,Standard_DS5_v2,Standard_DS11-1_v2,Standard_DS11_v2,Standard_DS12-1_v2,Standard_DS12-2_v2,Standard_DS12_v2,Standard_DS13-2_v2,Standard_DS13-4_v2,Standard_DS13_v2,Standard_DS14-4_v2,Standard_DS14-8_v2,Standard_DS14_v2,Standard_DS15_v2,Standard_DS2_v2_Promo,Standard_DS3_v2_Promo,Standard_DS4_v2_Promo,Standard_DS5_v2_Promo,Standard_DS11_v2_Promo,Standard_DS12_v2_Promo,Standard_DS13_v2_Promo,Standard_DS14_v2_Promo,Standard_F1s,Standard_F2s,Standard_F4s,Standard_F8s,Standard_F16s,Standard_D2s_v3,Standard_D4s_v3,Standard_D8s_v3,Standard_D16s_v3,Standard_D32s_v3,Standard_D2a_v4,Standard_D4a_v4,Standard_D8a_v4,Standard_D16a_v4,Standard_D32a_v4,Standard_D48a_v4,Standard_D64a_v4,Standard_D96a_v4,Standard_D2as_v4,Standard_D4as_v4,Standard_D8as_v4,Standard_D16as_v4,Standard_D32as_v4,Standard_D48as_v4,Standard_D64as_v4,Standard_D96as_v4,Standard_E2a_v4,Standard_E4a_v4,Standard_E8a_v4,Standard_E16a_v4,Standard_E20a_v4,Standard_E32a_v4,Standard_E48a_v4,Standard_E64a_v4,Standard_E96a_v4,Standard_E2as_v4,Standard_E4-2as_v4,Standard_E4as_v4,Standard_E8-2as_v4,Standard_E8-4as_v4,Standard_E8as_v4,Standard_E16-4as_v4,Standard_E16-8as_v4,Standard_E16as_v4,Standard_E20as_v4,Standard_E32-8as_v4,Standard_E32-16as_v4,Standard_E32as_v4,Standard_E48as_v4,Standard_E64-16as_v4,Standard_E64-32as_v4,Standard_E64as_v4,Standard_E96-24as_v4,Standard_E96-48as_v4,Standard_E96as_v4,Standard_D1_v2,Standard_D2_v2,Standard_D3_v2,Standard_D4_v2,Standard_D5_v2,Standard_D11_v2,Standard_D12_v2,Standard_D13_v2,Standard_D14_v2,Standard_D15_v2,Standard_D2_v2_Promo,Standard_D3_v2_Promo,Standard_D4_v2_Promo,Standard_D5_v2_Promo,Standard_D11_v2_Promo,Standard_D12_v2_Promo,Standard_D13_v2_Promo,Standard_D14_v2_Promo,Standard_F1,Standard_F2,Standard_F4,Standard_F8,Standard_F16,Standard_A1_v2,Standard_A2m_v2,Standard_A2_v2,Standard_A4m_v2,Standard_A4_v2,Standard_A8m_v2,Standard_A8_v2,Standard_D2_v3,Standard_D4_v3,Standard_D8_v3,Standard_D16_v3,Standard_D32_v3,Standard_D48_v3,Standard_D64_v3,Standard_D48s_v3,Standard_D64s_v3,Standard_E2_v3,Standard_E4_v3,Standard_E8_v3,Standard_E16_v3,Standard_E20_v3,Standard_E32_v3,Standard_E48_v3,Standard_E64_v3,Standard_E2s_v3,Standard_E4-2s_v3,Standard_E4s_v3,Standard_E8-2s_v3,Standard_E8-4s_v3,Standard_E8s_v3,Standard_E16-4s_v3,Standard_E16-8s_v3,Standard_E16s_v3,Standard_E20s_v3,Standard_E32-8s_v3,Standard_E32-16s_v3,Standard_E32s_v3,Standard_E48s_v3,Standard_E64-16s_v3,Standard_E64-32s_v3,Standard_E64s_v3,Standard_A0,Standard_A1,Standard_A2,Standard_A3,Standard_A5,Standard_A4,Standard_A6,Standard_A7,Basic_A0,Basic_A1,Basic_A2,Basic_A3,Basic_A4,Standard_E64i_v3,Standard_E64is_v3,Standard_M208ms_v2,Standard_M208s_v2,Standard_M416-208s_v2,Standard_M416s_v2,Standard_M416-208ms_v2,Standard_M416ms_v2,Standard_H8,Standard_H8_Promo,Standard_H16,Standard_H16_Promo,Standard_H8m,Standard_H8m_Promo,Standard_H16m,Standard_H16m_Promo,Standard_H16r,Standard_H16r_Promo,Standard_H16mr,Standard_H16mr_Promo,Standard_D1,Standard_D2,Standard_D3,Standard_D4,Standard_D11,Standard_D12,Standard_D13,Standard_D14,Standard_NV6,Standard_NV12,Standard_NV24,Standard_NV6_Promo,Standard_NV12_Promo,Standard_NV24_Promo,Standard_NC4as_T4_v3,Standard_NC8as_T4_v3,Standard_NC16as_T4_v3,Standard_NC64as_T4_v3,Standard_NV6s_v2,Standard_NV12s_v2,Standard_NV24s_v2,Standard_NV12s_v3,Standard_NV24s_v3,Standard_NV48s_v3,Standard_HB120rs_v2,Standard_D2ds_v4,Standard_D4ds_v4,Standard_D8ds_v4,Standard_D16ds_v4,Standard_D32ds_v4,Standard_D48ds_v4,Standard_D64ds_v4,Standard_D2ds_v5,Standard_D4ds_v5,Standard_D8ds_v5,Standard_D16ds_v5,Standard_D32ds_v5,Standard_D48ds_v5,Standard_D64ds_v5,Standard_D96ds_v5,Standard_D2d_v4,Standard_D4d_v4,Standard_D8d_v4,Standard_D16d_v4,Standard_D32d_v4,Standard_D48d_v4,Standard_D64d_v4,Standard_D2d_v5,Standard_D4d_v5,Standard_D8d_v5,Standard_D16d_v5,Standard_D32d_v5,Standard_D48d_v5,Standard_D64d_v5,Standard_D96d_v5,Standard_D2s_v4,Standard_D4s_v4,Standard_D8s_v4,Standard_D16s_v4,Standard_D32s_v4,Standard_D48s_v4,Standard_D64s_v4,Standard_D2s_v5,Standard_D4s_v5,Standard_D8s_v5,Standard_D16s_v5,Standard_D32s_v5,Standard_D48s_v5,Standard_D64s_v5,Standard_D96s_v5,Standard_D2_v4,Standard_D4_v4,Standard_D8_v4,Standard_D16_v4,Standard_D32_v4,Standard_D48_v4,Standard_D64_v4,Standard_D2_v5,Standard_D4_v5,Standard_D8_v5,Standard_D16_v5,Standard_D32_v5,Standard_D48_v5,Standard_D64_v5,Standard_D96_v5,Standard_E2ds_v4,Standard_E4-2ds_v4,Standard_E4ds_v4,Standard_E8-2ds_v4,Standard_E8-4ds_v4,Standard_E8ds_v4,Standard_E16-4ds_v4,Standard_E16-8ds_v4,Standard_E16ds_v4,Standard_E20ds_v4,Standard_E32-8ds_v4,Standard_E32-16ds_v4,Standard_E32ds_v4,Standard_E48ds_v4,Standard_E64-16ds_v4,Standard_E64-32ds_v4,Standard_E64ds_v4,Standard_E80ids_v4,Standard_E2ds_v5,Standard_E4-2ds_v5,Standard_E4ds_v5,Standard_E8-2ds_v5,Standard_E8-4ds_v5,Standard_E8ds_v5,Standard_E16-4ds_v5,Standard_E16-8ds_v5,Standard_E16ds_v5,Standard_E20ds_v5,Standard_E32-8ds_v5,Standard_E32-16ds_v5,Standard_E32ds_v5,Standard_E48ds_v5,Standard_E64-16ds_v5,Standard_E64-32ds_v5,Standard_E64ds_v5,Standard_E96-24ds_v5,Standard_E96-48ds_v5,Standard_E96ds_v5,Standard_E104ids_v5,Standard_E2d_v4,Standard_E4d_v4,Standard_E8d_v4,Standard_E16d_v4,Standard_E20d_v4,Standard_E32d_v4,Standard_E48d_v4,Standard_E64d_v4,Standard_E2d_v5,Standard_E4d_v5,Standard_E8d_v5,Standard_E16d_v5,Standard_E20d_v5,Standard_E32d_v5,Standard_E48d_v5,Standard_E64d_v5,Standard_E96d_v5,Standard_E104id_v5,Standard_E2s_v4,Standard_E4-2s_v4,Standard_E4s_v4,Standard_E8-2s_v4,Standard_E8-4s_v4,Standard_E8s_v4,Standard_E16-4s_v4,Standard_E16-8s_v4,Standard_E16s_v4,Standard_E20s_v4,Standard_E32-8s_v4,Standard_E32-16s_v4,Standard_E32s_v4,Standard_E48s_v4,Standard_E64-16s_v4,Standard_E64-32s_v4,Standard_E64s_v4,Standard_E80is_v4,Standard_E2s_v5,Standard_E4-2s_v5,Standard_E4s_v5,Standard_E8-2s_v5,Standard_E8-4s_v5,Standard_E8s_v5,Standard_E16-4s_v5,Standard_E16-8s_v5,Standard_E16s_v5,Standard_E20s_v5,Standard_E32-8s_v5,Standard_E32-16s_v5,Standard_E32s_v5,Standard_E48s_v5,Standard_E64-16s_v5,Standard_E64-32s_v5,Standard_E64s_v5,Standard_E96-24s_v5,Standard_E96-48s_v5,Standard_E96s_v5,Standard_E104is_v5,Standard_E2_v4,Standard_E4_v4,Standard_E8_v4,Standard_E16_v4,Standard_E20_v4,Standard_E32_v4,Standard_E48_v4,Standard_E64_v4,Standard_E2_v5,Standard_E4_v5,Standard_E8_v5,Standard_E16_v5,Standard_E20_v5,Standard_E32_v5,Standard_E48_v5,Standard_E64_v5,Standard_E96_v5,Standard_E104i_v5,Standard_F2s_v2,Standard_F4s_v2,Standard_F8s_v2,Standard_F16s_v2,Standard_F32s_v2,Standard_F48s_v2,Standard_F64s_v2,Standard_F72s_v2,Standard_NC6s_v2,Standard_NC12s_v2,Standard_NC24rs_v2,Standard_NC24s_v2,Standard_NC6,Standard_NC12,Standard_NC24,Standard_NC24r,Standard_NC6_Promo,Standard_NC12_Promo,Standard_NC24_Promo,Standard_NC24r_Promo,Standard_DS1,Standard_DS2,Standard_DS3,Standard_DS4,Standard_DS11,Standard_DS12,Standard_DS13,Standard_DS14,Standard_L8s_v2,Standard_L16s_v2,Standard_L32s_v2,Standard_L48s_v2,Standard_L64s_v2,Standard_L80s_v2,Standard_M64,Standard_M64m,Standard_M128,Standard_M128m,Standard_M8-2ms,Standard_M8-4ms,Standard_M8ms,Standard_M16-4ms,Standard_M16-8ms,Standard_M16ms,Standard_M32-8ms,Standard_M32-16ms,Standard_M32ls,Standard_M32ms,Standard_M32ts,Standard_M64-16ms,Standard_M64-32ms,Standard_M64ls,Standard_M64ms,Standard_M64s,Standard_M128-32ms,Standard_M128-64ms,Standard_M128ms,Standard_M128s,Standard_M32ms_v2,Standard_M64ms_v2,Standard_M64s_v2,Standard_M128ms_v2,Standard_M128s_v2,Standard_M192ims_v2,Standard_M192is_v2,Standard_M32dms_v2,Standard_M64dms_v2,Standard_M64ds_v2,Standard_M128dms_v2,Standard_M128ds_v2,Standard_M192idms_v2,Standard_M192ids_v2,Standard_DC8_v2,Standard_DC1s_v2,Standard_DC2s_v2,Standard_DC4s_v2,Standard_ND40rs_v2,Standard_FX4mds,Standard_FX12mds,Standard_FX24mds,Standard_FX36mds,Standard_FX48mds,Standard_NP10s,Standard_NP20s,Standard_NP40s,Standard_D2as_v5,Standard_D4as_v5,Standard_D8as_v5,Standard_D16as_v5,Standard_D32as_v5,Standard_D48as_v5,Standard_D64as_v5,Standard_D96as_v5,Standard_E2as_v5,Standard_E4-2as_v5,Standard_E4as_v5,Standard_E8-2as_v5,Standard_E8-4as_v5,Standard_E8as_v5,Standard_E16-4as_v5,Standard_E16-8as_v5,Standard_E16as_v5,Standard_E20as_v5,Standard_E32-8as_v5,Standard_E32-16as_v5,Standard_E32as_v5,Standard_E48as_v5,Standard_E64-16as_v5,Standard_E64-32as_v5,Standard_E64as_v5,Standard_E96-24as_v5,Standard_E96-48as_v5,Standard_E96as_v5,Standard_D2ads_v5,Standard_D4ads_v5,Standard_D8ads_v5,Standard_D16ads_v5,Standard_D32ads_v5,Standard_D48ads_v5,Standard_D64ads_v5,Standard_D96ads_v5,Standard_E2ads_v5,Standard_E4-2ads_v5,Standard_E4ads_v5,Standard_E8-2ads_v5,Standard_E8-4ads_v5,Standard_E8ads_v5,Standard_E16-4ads_v5,Standard_E16-8ads_v5,Standard_E16ads_v5,Standard_E20ads_v5,Standard_E32-8ads_v5,Standard_E32-16ads_v5,Standard_E32ads_v5,Standard_E48ads_v5,Standard_E64-16ads_v5,Standard_E64-32ads_v5,Standard_E64ads_v5,Standard_E96-24ads_v5,Standard_E96-48ads_v5,Standard_E96ads_v5,Standard_HC44rs,Standard_ND6s,Standard_ND12s,Standard_ND24rs,Standard_ND24s,Standard_DC2s,Standard_DC4s,Standard_HB120-16rs_v3,Standard_HB120-32rs_v3,Standard_HB120-64rs_v3,Standard_HB120-96rs_v3,Standard_HB120rs_v3,Standard_NV4as_v4,Standard_NV8as_v4,Standard_NV16as_v4,Standard_NV32as_v4,Standard_NC6s_v3,Standard_NC12s_v3,Standard_NC24rs_v3,Standard_NC24s_v3,Standard_PB6s,Standard_HB60rs,Standard_ND96asr_v4,Standard_ND40s_v3. Find out more on the valid VM sizes in each region at https://aka.ms/azure-regions.
Code: InvalidParameter
Message: The value [Standard_DS4_v2].name provided for the VM size is not valid. The valid sizes in the current region are: Standard_B1ls,Standard_B1ms,Standard_B1s,Standard_B2ms,Standard_B2s,Standard_B4ms,Standard_B8ms,Standard_B12ms,Standard_B16ms,Standard_B20ms,Standard_DS1_v2,Standard_DS2_v2,Standard_DS3_v2,Standard_DS4_v2,Standard_DS5_v2,Standard_DS11-1_v2,Standard_DS11_v2,Standard_DS12-1_v2,Standard_DS12-2_v2,Standard_DS12_v2,Standard_DS13-2_v2,Standard_DS13-4_v2,Standard_DS13_v2,Standard_DS14-4_v2,Standard_DS14-8_v2,Standard_DS14_v2,Standard_DS15_v2,Standard_DS2_v2_Promo,Standard_DS3_v2_Promo,Standard_DS4_v2_Promo,Standard_DS5_v2_Promo,Standard_DS11_v2_Promo,Standard_DS12_v2_Promo,Standard_DS13_v2_Promo,Standard_DS14_v2_Promo,Standard_F1s,Standard_F2s,Standard_F4s,Standard_F8s,Standard_F16s,Standard_D2s_v3,Standard_D4s_v3,Standard_D8s_v3,Standard_D16s_v3,Standard_D32s_v3,Standard_D2a_v4,Standard_D4a_v4,Standard_D8a_v4,Standard_D16a_v4,Standard_D32a_v4,Standard_D48a_v4,Standard_D64a_v4,Standard_D96a_v4,Standard_D2as_v4,Standard_D4as_v4,Standard_D8as_v4,Standard_D16as_v4,Standard_D32as_v4,Standard_D48as_v4,Standard_D64as_v4,Standard_D96as_v4,Standard_E2a_v4,Standard_E4a_v4,Standard_E8a_v4,Standard_E16a_v4,Standard_E20a_v4,Standard_E32a_v4,Standard_E48a_v4,Standard_E64a_v4,Standard_E96a_v4,Standard_E2as_v4,Standard_E4-2as_v4,Standard_E4as_v4,Standard_E8-2as_v4,Standard_E8-4as_v4,Standard_E8as_v4,Standard_E16-4as_v4,Standard_E16-8as_v4,Standard_E16as_v4,Standard_E20as_v4,Standard_E32-8as_v4,Standard_E32-16as_v4,Standard_E32as_v4,Standard_E48as_v4,Standard_E64-16as_v4,Standard_E64-32as_v4,Standard_E64as_v4,Standard_E96-24as_v4,Standard_E96-48as_v4,Standard_E96as_v4,Standard_D1_v2,Standard_D2_v2,Standard_D3_v2,Standard_D4_v2,Standard_D5_v2,Standard_D11_v2,Standard_D12_v2,Standard_D13_v2,Standard_D14_v2,Standard_D15_v2,Standard_D2_v2_Promo,Standard_D3_v2_Promo,Standard_D4_v2_Promo,Standard_D5_v2_Promo,Standard_D11_v2_Promo,Standard_D12_v2_Promo,Standard_D13_v2_Promo,Standard_D14_v2_Promo,Standard_F1,Standard_F2,Standard_F4,Standard_F8,Standard_F16,Standard_A1_v2,Standard_A2m_v2,Standard_A2_v2,Standard_A4m_v2,Standard_A4_v2,Standard_A8m_v2,Standard_A8_v2,Standard_D2_v3,Standard_D4_v3,Standard_D8_v3,Standard_D16_v3,Standard_D32_v3,Standard_D48_v3,Standard_D64_v3,Standard_D48s_v3,Standard_D64s_v3,Standard_E2_v3,Standard_E4_v3,Standard_E8_v3,Standard_E16_v3,Standard_E20_v3,Standard_E32_v3,Standard_E48_v3,Standard_E64_v3,Standard_E2s_v3,Standard_E4-2s_v3,Standard_E4s_v3,Standard_E8-2s_v3,Standard_E8-4s_v3,Standard_E8s_v3,Standard_E16-4s_v3,Standard_E16-8s_v3,Standard_E16s_v3,Standard_E20s_v3,Standard_E32-8s_v3,Standard_E32-16s_v3,Standard_E32s_v3,Standard_E48s_v3,Standard_E64-16s_v3,Standard_E64-32s_v3,Standard_E64s_v3,Standard_A0,Standard_A1,Standard_A2,Standard_A3,Standard_A5,Standard_A4,Standard_A6,Standard_A7,Basic_A0,Basic_A1,Basic_A2,Basic_A3,Basic_A4,Standard_E64i_v3,Standard_E64is_v3,Standard_M208ms_v2,Standard_M208s_v2,Standard_M416-208s_v2,Standard_M416s_v2,Standard_M416-208ms_v2,Standard_M416ms_v2,Standard_H8,Standard_H8_Promo,Standard_H16,Standard_H16_Promo,Standard_H8m,Standard_H8m_Promo,Standard_H16m,Standard_H16m_Promo,Standard_H16r,Standard_H16r_Promo,Standard_H16mr,Standard_H16mr_Promo,Standard_D1,Standard_D2,Standard_D3,Standard_D4,Standard_D11,Standard_D12,Standard_D13,Standard_D14,Standard_NV6,Standard_NV12,Standard_NV24,Standard_NV6_Promo,Standard_NV12_Promo,Standard_NV24_Promo,Standard_NC4as_T4_v3,Standard_NC8as_T4_v3,Standard_NC16as_T4_v3,Standard_NC64as_T4_v3,Standard_NV6s_v2,Standard_NV12s_v2,Standard_NV24s_v2,Standard_NV12s_v3,Standard_NV24s_v3,Standard_NV48s_v3,Standard_HB120rs_v2,Standard_D2ds_v4,Standard_D4ds_v4,Standard_D8ds_v4,Standard_D16ds_v4,Standard_D32ds_v4,Standard_D48ds_v4,Standard_D64ds_v4,Standard_D2ds_v5,Standard_D4ds_v5,Standard_D8ds_v5,Standard_D16ds_v5,Standard_D32ds_v5,Standard_D48ds_v5,Standard_D64ds_v5,Standard_D96ds_v5,Standard_D2d_v4,Standard_D4d_v4,Standard_D8d_v4,Standard_D16d_v4,Standard_D32d_v4,Standard_D48d_v4,Standard_D64d_v4,Standard_D2d_v5,Standard_D4d_v5,Standard_D8d_v5,Standard_D16d_v5,Standard_D32d_v5,Standard_D48d_v5,Standard_D64d_v5,Standard_D96d_v5,Standard_D2s_v4,Standard_D4s_v4,Standard_D8s_v4,Standard_D16s_v4,Standard_D32s_v4,Standard_D48s_v4,Standard_D64s_v4,Standard_D2s_v5,Standard_D4s_v5,Standard_D8s_v5,Standard_D16s_v5,Standard_D32s_v5,Standard_D48s_v5,Standard_D64s_v5,Standard_D96s_v5,Standard_D2_v4,Standard_D4_v4,Standard_D8_v4,Standard_D16_v4,Standard_D32_v4,Standard_D48_v4,Standard_D64_v4,Standard_D2_v5,Standard_D4_v5,Standard_D8_v5,Standard_D16_v5,Standard_D32_v5,Standard_D48_v5,Standard_D64_v5,Standard_D96_v5,Standard_E2ds_v4,Standard_E4-2ds_v4,Standard_E4ds_v4,Standard_E8-2ds_v4,Standard_E8-4ds_v4,Standard_E8ds_v4,Standard_E16-4ds_v4,Standard_E16-8ds_v4,Standard_E16ds_v4,Standard_E20ds_v4,Standard_E32-8ds_v4,Standard_E32-16ds_v4,Standard_E32ds_v4,Standard_E48ds_v4,Standard_E64-16ds_v4,Standard_E64-32ds_v4,Standard_E64ds_v4,Standard_E80ids_v4,Standard_E2ds_v5,Standard_E4-2ds_v5,Standard_E4ds_v5,Standard_E8-2ds_v5,Standard_E8-4ds_v5,Standard_E8ds_v5,Standard_E16-4ds_v5,Standard_E16-8ds_v5,Standard_E16ds_v5,Standard_E20ds_v5,Standard_E32-8ds_v5,Standard_E32-16ds_v5,Standard_E32ds_v5,Standard_E48ds_v5,Standard_E64-16ds_v5,Standard_E64-32ds_v5,Standard_E64ds_v5,Standard_E96-24ds_v5,Standard_E96-48ds_v5,Standard_E96ds_v5,Standard_E104ids_v5,Standard_E2d_v4,Standard_E4d_v4,Standard_E8d_v4,Standard_E16d_v4,Standard_E20d_v4,Standard_E32d_v4,Standard_E48d_v4,Standard_E64d_v4,Standard_E2d_v5,Standard_E4d_v5,Standard_E8d_v5,Standard_E16d_v5,Standard_E20d_v5,Standard_E32d_v5,Standard_E48d_v5,Standard_E64d_v5,Standard_E96d_v5,Standard_E104id_v5,Standard_E2s_v4,Standard_E4-2s_v4,Standard_E4s_v4,Standard_E8-2s_v4,Standard_E8-4s_v4,Standard_E8s_v4,Standard_E16-4s_v4,Standard_E16-8s_v4,Standard_E16s_v4,Standard_E20s_v4,Standard_E32-8s_v4,Standard_E32-16s_v4,Standard_E32s_v4,Standard_E48s_v4,Standard_E64-16s_v4,Standard_E64-32s_v4,Standard_E64s_v4,Standard_E80is_v4,Standard_E2s_v5,Standard_E4-2s_v5,Standard_E4s_v5,Standard_E8-2s_v5,Standard_E8-4s_v5,Standard_E8s_v5,Standard_E16-4s_v5,Standard_E16-8s_v5,Standard_E16s_v5,Standard_E20s_v5,Standard_E32-8s_v5,Standard_E32-16s_v5,Standard_E32s_v5,Standard_E48s_v5,Standard_E64-16s_v5,Standard_E64-32s_v5,Standard_E64s_v5,Standard_E96-24s_v5,Standard_E96-48s_v5,Standard_E96s_v5,Standard_E104is_v5,Standard_E2_v4,Standard_E4_v4,Standard_E8_v4,Standard_E16_v4,Standard_E20_v4,Standard_E32_v4,Standard_E48_v4,Standard_E64_v4,Standard_E2_v5,Standard_E4_v5,Standard_E8_v5,Standard_E16_v5,Standard_E20_v5,Standard_E32_v5,Standard_E48_v5,Standard_E64_v5,Standard_E96_v5,Standard_E104i_v5,Standard_F2s_v2,Standard_F4s_v2,Standard_F8s_v2,Standard_F16s_v2,Standard_F32s_v2,Standard_F48s_v2,Standard_F64s_v2,Standard_F72s_v2,Standard_NC6s_v2,Standard_NC12s_v2,Standard_NC24rs_v2,Standard_NC24s_v2,Standard_NC6,Standard_NC12,Standard_NC24,Standard_NC24r,Standard_NC6_Promo,Standard_NC12_Promo,Standard_NC24_Promo,Standard_NC24r_Promo,Standard_DS1,Standard_DS2,Standard_DS3,Standard_DS4,Standard_DS11,Standard_DS12,Standard_DS13,Standard_DS14,Standard_L8s_v2,Standard_L16s_v2,Standard_L32s_v2,Standard_L48s_v2,Standard_L64s_v2,Standard_L80s_v2,Standard_M64,Standard_M64m,Standard_M128,Standard_M128m,Standard_M8-2ms,Standard_M8-4ms,Standard_M8ms,Standard_M16-4ms,Standard_M16-8ms,Standard_M16ms,Standard_M32-8ms,Standard_M32-16ms,Standard_M32ls,Standard_M32ms,Standard_M32ts,Standard_M64-16ms,Standard_M64-32ms,Standard_M64ls,Standard_M64ms,Standard_M64s,Standard_M128-32ms,Standard_M128-64ms,Standard_M128ms,Standard_M128s,Standard_M32ms_v2,Standard_M64ms_v2,Standard_M64s_v2,Standard_M128ms_v2,Standard_M128s_v2,Standard_M192ims_v2,Standard_M192is_v2,Standard_M32dms_v2,Standard_M64dms_v2,Standard_M64ds_v2,Standard_M128dms_v2,Standard_M128ds_v2,Standard_M192idms_v2,Standard_M192ids_v2,Standard_DC8_v2,Standard_DC1s_v2,Standard_DC2s_v2,Standard_DC4s_v2,Standard_ND40rs_v2,Standard_FX4mds,Standard_FX12mds,Standard_FX24mds,Standard_FX36mds,Standard_FX48mds,Standard_NP10s,Standard_NP20s,Standard_NP40s,Standard_D2as_v5,Standard_D4as_v5,Standard_D8as_v5,Standard_D16as_v5,Standard_D32as_v5,Standard_D48as_v5,Standard_D64as_v5,Standard_D96as_v5,Standard_E2as_v5,Standard_E4-2as_v5,Standard_E4as_v5,Standard_E8-2as_v5,Standard_E8-4as_v5,Standard_E8as_v5,Standard_E16-4as_v5,Standard_E16-8as_v5,Standard_E16as_v5,Standard_E20as_v5,Standard_E32-8as_v5,Standard_E32-16as_v5,Standard_E32as_v5,Standard_E48as_v5,Standard_E64-16as_v5,Standard_E64-32as_v5,Standard_E64as_v5,Standard_E96-24as_v5,Standard_E96-48as_v5,Standard_E96as_v5,Standard_D2ads_v5,Standard_D4ads_v5,Standard_D8ads_v5,Standard_D16ads_v5,Standard_D32ads_v5,Standard_D48ads_v5,Standard_D64ads_v5,Standard_D96ads_v5,Standard_E2ads_v5,Standard_E4-2ads_v5,Standard_E4ads_v5,Standard_E8-2ads_v5,Standard_E8-4ads_v5,Standard_E8ads_v5,Standard_E16-4ads_v5,Standard_E16-8ads_v5,Standard_E16ads_v5,Standard_E20ads_v5,Standard_E32-8ads_v5,Standard_E32-16ads_v5,Standard_E32ads_v5,Standard_E48ads_v5,Standard_E64-16ads_v5,Standard_E64-32ads_v5,Standard_E64ads_v5,Standard_E96-24ads_v5,Standard_E96-48ads_v5,Standard_E96ads_v5,Standard_HC44rs,Standard_ND6s,Standard_ND12s,Standard_ND24rs,Standard_ND24s,Standard_DC2s,Standard_DC4s,Standard_HB120-16rs_v3,Standard_HB120-32rs_v3,Standard_HB120-64rs_v3,Standard_HB120-96rs_v3,Standard_HB120rs_v3,Standard_NV4as_v4,Standard_NV8as_v4,Standard_NV16as_v4,Standard_NV32as_v4,Standard_NC6s_v3,Standard_NC12s_v3,Standard_NC24rs_v3,Standard_NC24s_v3,Standard_PB6s,Standard_HB60rs,Standard_ND96asr_v4,Standard_ND40s_v3. Find out more on the valid VM sizes in each region at https://aka.ms/azure-regions.
Target: vmSize
yetunde@Azure:~$ az vm resize --resource-group ytarg --name webserver --size [Standard_DS1_v2].name
(InvalidParameter) The value [Standard_DS1_v2].name provided for the VM size is not valid. The valid sizes in the current region are: Standard_B1ls,Standard_B1ms,Standard_B1s,Standard_B2ms,Standard_B2s,Standard_B4ms,Standard_B8ms,Standard_B12ms,Standard_B16ms,Standard_B20ms,Standard_DS1_v2,Standard_DS2_v2,Standard_DS3_v2,Standard_DS4_v2,Standard_DS5_v2,Standard_DS11-1_v2,Standard_DS11_v2,Standard_DS12-1_v2,Standard_DS12-2_v2,Standard_DS12_v2,Standard_DS13-2_v2,Standard_DS13-4_v2,Standard_DS13_v2,Standard_DS14-4_v2,Standard_DS14-8_v2,Standard_DS14_v2,Standard_DS15_v2,Standard_DS2_v2_Promo,Standard_DS3_v2_Promo,Standard_DS4_v2_Promo,Standard_DS5_v2_Promo,Standard_DS11_v2_Promo,Standard_DS12_v2_Promo,Standard_DS13_v2_Promo,Standard_DS14_v2_Promo,Standard_F1s,Standard_F2s,Standard_F4s,Standard_F8s,Standard_F16s,Standard_D2s_v3,Standard_D4s_v3,Standard_D8s_v3,Standard_D16s_v3,Standard_D32s_v3,Standard_D2a_v4,Standard_D4a_v4,Standard_D8a_v4,Standard_D16a_v4,Standard_D32a_v4,Standard_D48a_v4,Standard_D64a_v4,Standard_D96a_v4,Standard_D2as_v4,Standard_D4as_v4,Standard_D8as_v4,Standard_D16as_v4,Standard_D32as_v4,Standard_D48as_v4,Standard_D64as_v4,Standard_D96as_v4,Standard_E2a_v4,Standard_E4a_v4,Standard_E8a_v4,Standard_E16a_v4,Standard_E20a_v4,Standard_E32a_v4,Standard_E48a_v4,Standard_E64a_v4,Standard_E96a_v4,Standard_E2as_v4,Standard_E4-2as_v4,Standard_E4as_v4,Standard_E8-2as_v4,Standard_E8-4as_v4,Standard_E8as_v4,Standard_E16-4as_v4,Standard_E16-8as_v4,Standard_E16as_v4,Standard_E20as_v4,Standard_E32-8as_v4,Standard_E32-16as_v4,Standard_E32as_v4,Standard_E48as_v4,Standard_E64-16as_v4,Standard_E64-32as_v4,Standard_E64as_v4,Standard_E96-24as_v4,Standard_E96-48as_v4,Standard_E96as_v4,Standard_D1_v2,Standard_D2_v2,Standard_D3_v2,Standard_D4_v2,Standard_D5_v2,Standard_D11_v2,Standard_D12_v2,Standard_D13_v2,Standard_D14_v2,Standard_D15_v2,Standard_D2_v2_Promo,Standard_D3_v2_Promo,Standard_D4_v2_Promo,Standard_D5_v2_Promo,Standard_D11_v2_Promo,Standard_D12_v2_Promo,Standard_D13_v2_Promo,Standard_D14_v2_Promo,Standard_F1,Standard_F2,Standard_F4,Standard_F8,Standard_F16,Standard_A1_v2,Standard_A2m_v2,Standard_A2_v2,Standard_A4m_v2,Standard_A4_v2,Standard_A8m_v2,Standard_A8_v2,Standard_D2_v3,Standard_D4_v3,Standard_D8_v3,Standard_D16_v3,Standard_D32_v3,Standard_D48_v3,Standard_D64_v3,Standard_D48s_v3,Standard_D64s_v3,Standard_E2_v3,Standard_E4_v3,Standard_E8_v3,Standard_E16_v3,Standard_E20_v3,Standard_E32_v3,Standard_E48_v3,Standard_E64_v3,Standard_E2s_v3,Standard_E4-2s_v3,Standard_E4s_v3,Standard_E8-2s_v3,Standard_E8-4s_v3,Standard_E8s_v3,Standard_E16-4s_v3,Standard_E16-8s_v3,Standard_E16s_v3,Standard_E20s_v3,Standard_E32-8s_v3,Standard_E32-16s_v3,Standard_E32s_v3,Standard_E48s_v3,Standard_E64-16s_v3,Standard_E64-32s_v3,Standard_E64s_v3,Standard_A0,Standard_A1,Standard_A2,Standard_A3,Standard_A5,Standard_A4,Standard_A6,Standard_A7,Basic_A0,Basic_A1,Basic_A2,Basic_A3,Basic_A4,Standard_E64i_v3,Standard_E64is_v3,Standard_M208ms_v2,Standard_M208s_v2,Standard_M416-208s_v2,Standard_M416s_v2,Standard_M416-208ms_v2,Standard_M416ms_v2,Standard_H8,Standard_H8_Promo,Standard_H16,Standard_H16_Promo,Standard_H8m,Standard_H8m_Promo,Standard_H16m,Standard_H16m_Promo,Standard_H16r,Standard_H16r_Promo,Standard_H16mr,Standard_H16mr_Promo,Standard_D1,Standard_D2,Standard_D3,Standard_D4,Standard_D11,Standard_D12,Standard_D13,Standard_D14,Standard_NV6,Standard_NV12,Standard_NV24,Standard_NV6_Promo,Standard_NV12_Promo,Standard_NV24_Promo,Standard_NC4as_T4_v3,Standard_NC8as_T4_v3,Standard_NC16as_T4_v3,Standard_NC64as_T4_v3,Standard_NV6s_v2,Standard_NV12s_v2,Standard_NV24s_v2,Standard_NV12s_v3,Standard_NV24s_v3,Standard_NV48s_v3,Standard_HB120rs_v2,Standard_D2ds_v4,Standard_D4ds_v4,Standard_D8ds_v4,Standard_D16ds_v4,Standard_D32ds_v4,Standard_D48ds_v4,Standard_D64ds_v4,Standard_D2ds_v5,Standard_D4ds_v5,Standard_D8ds_v5,Standard_D16ds_v5,Standard_D32ds_v5,Standard_D48ds_v5,Standard_D64ds_v5,Standard_D96ds_v5,Standard_D2d_v4,Standard_D4d_v4,Standard_D8d_v4,Standard_D16d_v4,Standard_D32d_v4,Standard_D48d_v4,Standard_D64d_v4,Standard_D2d_v5,Standard_D4d_v5,Standard_D8d_v5,Standard_D16d_v5,Standard_D32d_v5,Standard_D48d_v5,Standard_D64d_v5,Standard_D96d_v5,Standard_D2s_v4,Standard_D4s_v4,Standard_D8s_v4,Standard_D16s_v4,Standard_D32s_v4,Standard_D48s_v4,Standard_D64s_v4,Standard_D2s_v5,Standard_D4s_v5,Standard_D8s_v5,Standard_D16s_v5,Standard_D32s_v5,Standard_D48s_v5,Standard_D64s_v5,Standard_D96s_v5,Standard_D2_v4,Standard_D4_v4,Standard_D8_v4,Standard_D16_v4,Standard_D32_v4,Standard_D48_v4,Standard_D64_v4,Standard_D2_v5,Standard_D4_v5,Standard_D8_v5,Standard_D16_v5,Standard_D32_v5,Standard_D48_v5,Standard_D64_v5,Standard_D96_v5,Standard_E2ds_v4,Standard_E4-2ds_v4,Standard_E4ds_v4,Standard_E8-2ds_v4,Standard_E8-4ds_v4,Standard_E8ds_v4,Standard_E16-4ds_v4,Standard_E16-8ds_v4,Standard_E16ds_v4,Standard_E20ds_v4,Standard_E32-8ds_v4,Standard_E32-16ds_v4,Standard_E32ds_v4,Standard_E48ds_v4,Standard_E64-16ds_v4,Standard_E64-32ds_v4,Standard_E64ds_v4,Standard_E80ids_v4,Standard_E2ds_v5,Standard_E4-2ds_v5,Standard_E4ds_v5,Standard_E8-2ds_v5,Standard_E8-4ds_v5,Standard_E8ds_v5,Standard_E16-4ds_v5,Standard_E16-8ds_v5,Standard_E16ds_v5,Standard_E20ds_v5,Standard_E32-8ds_v5,Standard_E32-16ds_v5,Standard_E32ds_v5,Standard_E48ds_v5,Standard_E64-16ds_v5,Standard_E64-32ds_v5,Standard_E64ds_v5,Standard_E96-24ds_v5,Standard_E96-48ds_v5,Standard_E96ds_v5,Standard_E104ids_v5,Standard_E2d_v4,Standard_E4d_v4,Standard_E8d_v4,Standard_E16d_v4,Standard_E20d_v4,Standard_E32d_v4,Standard_E48d_v4,Standard_E64d_v4,Standard_E2d_v5,Standard_E4d_v5,Standard_E8d_v5,Standard_E16d_v5,Standard_E20d_v5,Standard_E32d_v5,Standard_E48d_v5,Standard_E64d_v5,Standard_E96d_v5,Standard_E104id_v5,Standard_E2s_v4,Standard_E4-2s_v4,Standard_E4s_v4,Standard_E8-2s_v4,Standard_E8-4s_v4,Standard_E8s_v4,Standard_E16-4s_v4,Standard_E16-8s_v4,Standard_E16s_v4,Standard_E20s_v4,Standard_E32-8s_v4,Standard_E32-16s_v4,Standard_E32s_v4,Standard_E48s_v4,Standard_E64-16s_v4,Standard_E64-32s_v4,Standard_E64s_v4,Standard_E80is_v4,Standard_E2s_v5,Standard_E4-2s_v5,Standard_E4s_v5,Standard_E8-2s_v5,Standard_E8-4s_v5,Standard_E8s_v5,Standard_E16-4s_v5,Standard_E16-8s_v5,Standard_E16s_v5,Standard_E20s_v5,Standard_E32-8s_v5,Standard_E32-16s_v5,Standard_E32s_v5,Standard_E48s_v5,Standard_E64-16s_v5,Standard_E64-32s_v5,Standard_E64s_v5,Standard_E96-24s_v5,Standard_E96-48s_v5,Standard_E96s_v5,Standard_E104is_v5,Standard_E2_v4,Standard_E4_v4,Standard_E8_v4,Standard_E16_v4,Standard_E20_v4,Standard_E32_v4,Standard_E48_v4,Standard_E64_v4,Standard_E2_v5,Standard_E4_v5,Standard_E8_v5,Standard_E16_v5,Standard_E20_v5,Standard_E32_v5,Standard_E48_v5,Standard_E64_v5,Standard_E96_v5,Standard_E104i_v5,Standard_F2s_v2,Standard_F4s_v2,Standard_F8s_v2,Standard_F16s_v2,Standard_F32s_v2,Standard_F48s_v2,Standard_F64s_v2,Standard_F72s_v2,Standard_NC6s_v2,Standard_NC12s_v2,Standard_NC24rs_v2,Standard_NC24s_v2,Standard_NC6,Standard_NC12,Standard_NC24,Standard_NC24r,Standard_NC6_Promo,Standard_NC12_Promo,Standard_NC24_Promo,Standard_NC24r_Promo,Standard_DS1,Standard_DS2,Standard_DS3,Standard_DS4,Standard_DS11,Standard_DS12,Standard_DS13,Standard_DS14,Standard_L8s_v2,Standard_L16s_v2,Standard_L32s_v2,Standard_L48s_v2,Standard_L64s_v2,Standard_L80s_v2,Standard_M64,Standard_M64m,Standard_M128,Standard_M128m,Standard_M8-2ms,Standard_M8-4ms,Standard_M8ms,Standard_M16-4ms,Standard_M16-8ms,Standard_M16ms,Standard_M32-8ms,Standard_M32-16ms,Standard_M32ls,Standard_M32ms,Standard_M32ts,Standard_M64-16ms,Standard_M64-32ms,Standard_M64ls,Standard_M64ms,Standard_M64s,Standard_M128-32ms,Standard_M128-64ms,Standard_M128ms,Standard_M128s,Standard_M32ms_v2,Standard_M64ms_v2,Standard_M64s_v2,Standard_M128ms_v2,Standard_M128s_v2,Standard_M192ims_v2,Standard_M192is_v2,Standard_M32dms_v2,Standard_M64dms_v2,Standard_M64ds_v2,Standard_M128dms_v2,Standard_M128ds_v2,Standard_M192idms_v2,Standard_M192ids_v2,Standard_DC8_v2,Standard_DC1s_v2,Standard_DC2s_v2,Standard_DC4s_v2,Standard_ND40rs_v2,Standard_FX4mds,Standard_FX12mds,Standard_FX24mds,Standard_FX36mds,Standard_FX48mds,Standard_NP10s,Standard_NP20s,Standard_NP40s,Standard_D2as_v5,Standard_D4as_v5,Standard_D8as_v5,Standard_D16as_v5,Standard_D32as_v5,Standard_D48as_v5,Standard_D64as_v5,Standard_D96as_v5,Standard_E2as_v5,Standard_E4-2as_v5,Standard_E4as_v5,Standard_E8-2as_v5,Standard_E8-4as_v5,Standard_E8as_v5,Standard_E16-4as_v5,Standard_E16-8as_v5,Standard_E16as_v5,Standard_E20as_v5,Standard_E32-8as_v5,Standard_E32-16as_v5,Standard_E32as_v5,Standard_E48as_v5,Standard_E64-16as_v5,Standard_E64-32as_v5,Standard_E64as_v5,Standard_E96-24as_v5,Standard_E96-48as_v5,Standard_E96as_v5,Standard_D2ads_v5,Standard_D4ads_v5,Standard_D8ads_v5,Standard_D16ads_v5,Standard_D32ads_v5,Standard_D48ads_v5,Standard_D64ads_v5,Standard_D96ads_v5,Standard_E2ads_v5,Standard_E4-2ads_v5,Standard_E4ads_v5,Standard_E8-2ads_v5,Standard_E8-4ads_v5,Standard_E8ads_v5,Standard_E16-4ads_v5,Standard_E16-8ads_v5,Standard_E16ads_v5,Standard_E20ads_v5,Standard_E32-8ads_v5,Standard_E32-16ads_v5,Standard_E32ads_v5,Standard_E48ads_v5,Standard_E64-16ads_v5,Standard_E64-32ads_v5,Standard_E64ads_v5,Standard_E96-24ads_v5,Standard_E96-48ads_v5,Standard_E96ads_v5,Standard_HC44rs,Standard_ND6s,Standard_ND12s,Standard_ND24rs,Standard_ND24s,Standard_DC2s,Standard_DC4s,Standard_HB120-16rs_v3,Standard_HB120-32rs_v3,Standard_HB120-64rs_v3,Standard_HB120-96rs_v3,Standard_HB120rs_v3,Standard_NV4as_v4,Standard_NV8as_v4,Standard_NV16as_v4,Standard_NV32as_v4,Standard_NC6s_v3,Standard_NC12s_v3,Standard_NC24rs_v3,Standard_NC24s_v3,Standard_PB6s,Standard_HB60rs,Standard_ND96asr_v4,Standard_ND40s_v3. Find out more on the valid VM sizes in each region at https://aka.ms/azure-regions.
Code: InvalidParameter
Message: The value [Standard_DS1_v2].name provided for the VM size is not valid. The valid sizes in the current region are: Standard_B1ls,Standard_B1ms,Standard_B1s,Standard_B2ms,Standard_B2s,Standard_B4ms,Standard_B8ms,Standard_B12ms,Standard_B16ms,Standard_B20ms,Standard_DS1_v2,Standard_DS2_v2,Standard_DS3_v2,Standard_DS4_v2,Standard_DS5_v2,Standard_DS11-1_v2,Standard_DS11_v2,Standard_DS12-1_v2,Standard_DS12-2_v2,Standard_DS12_v2,Standard_DS13-2_v2,Standard_DS13-4_v2,Standard_DS13_v2,Standard_DS14-4_v2,Standard_DS14-8_v2,Standard_DS14_v2,Standard_DS15_v2,Standard_DS2_v2_Promo,Standard_DS3_v2_Promo,Standard_DS4_v2_Promo,Standard_DS5_v2_Promo,Standard_DS11_v2_Promo,Standard_DS12_v2_Promo,Standard_DS13_v2_Promo,Standard_DS14_v2_Promo,Standard_F1s,Standard_F2s,Standard_F4s,Standard_F8s,Standard_F16s,Standard_D2s_v3,Standard_D4s_v3,Standard_D8s_v3,Standard_D16s_v3,Standard_D32s_v3,Standard_D2a_v4,Standard_D4a_v4,Standard_D8a_v4,Standard_D16a_v4,Standard_D32a_v4,Standard_D48a_v4,Standard_D64a_v4,Standard_D96a_v4,Standard_D2as_v4,Standard_D4as_v4,Standard_D8as_v4,Standard_D16as_v4,Standard_D32as_v4,Standard_D48as_v4,Standard_D64as_v4,Standard_D96as_v4,Standard_E2a_v4,Standard_E4a_v4,Standard_E8a_v4,Standard_E16a_v4,Standard_E20a_v4,Standard_E32a_v4,Standard_E48a_v4,Standard_E64a_v4,Standard_E96a_v4,Standard_E2as_v4,Standard_E4-2as_v4,Standard_E4as_v4,Standard_E8-2as_v4,Standard_E8-4as_v4,Standard_E8as_v4,Standard_E16-4as_v4,Standard_E16-8as_v4,Standard_E16as_v4,Standard_E20as_v4,Standard_E32-8as_v4,Standard_E32-16as_v4,Standard_E32as_v4,Standard_E48as_v4,Standard_E64-16as_v4,Standard_E64-32as_v4,Standard_E64as_v4,Standard_E96-24as_v4,Standard_E96-48as_v4,Standard_E96as_v4,Standard_D1_v2,Standard_D2_v2,Standard_D3_v2,Standard_D4_v2,Standard_D5_v2,Standard_D11_v2,Standard_D12_v2,Standard_D13_v2,Standard_D14_v2,Standard_D15_v2,Standard_D2_v2_Promo,Standard_D3_v2_Promo,Standard_D4_v2_Promo,Standard_D5_v2_Promo,Standard_D11_v2_Promo,Standard_D12_v2_Promo,Standard_D13_v2_Promo,Standard_D14_v2_Promo,Standard_F1,Standard_F2,Standard_F4,Standard_F8,Standard_F16,Standard_A1_v2,Standard_A2m_v2,Standard_A2_v2,Standard_A4m_v2,Standard_A4_v2,Standard_A8m_v2,Standard_A8_v2,Standard_D2_v3,Standard_D4_v3,Standard_D8_v3,Standard_D16_v3,Standard_D32_v3,Standard_D48_v3,Standard_D64_v3,Standard_D48s_v3,Standard_D64s_v3,Standard_E2_v3,Standard_E4_v3,Standard_E8_v3,Standard_E16_v3,Standard_E20_v3,Standard_E32_v3,Standard_E48_v3,Standard_E64_v3,Standard_E2s_v3,Standard_E4-2s_v3,Standard_E4s_v3,Standard_E8-2s_v3,Standard_E8-4s_v3,Standard_E8s_v3,Standard_E16-4s_v3,Standard_E16-8s_v3,Standard_E16s_v3,Standard_E20s_v3,Standard_E32-8s_v3,Standard_E32-16s_v3,Standard_E32s_v3,Standard_E48s_v3,Standard_E64-16s_v3,Standard_E64-32s_v3,Standard_E64s_v3,Standard_A0,Standard_A1,Standard_A2,Standard_A3,Standard_A5,Standard_A4,Standard_A6,Standard_A7,Basic_A0,Basic_A1,Basic_A2,Basic_A3,Basic_A4,Standard_E64i_v3,Standard_E64is_v3,Standard_M208ms_v2,Standard_M208s_v2,Standard_M416-208s_v2,Standard_M416s_v2,Standard_M416-208ms_v2,Standard_M416ms_v2,Standard_H8,Standard_H8_Promo,Standard_H16,Standard_H16_Promo,Standard_H8m,Standard_H8m_Promo,Standard_H16m,Standard_H16m_Promo,Standard_H16r,Standard_H16r_Promo,Standard_H16mr,Standard_H16mr_Promo,Standard_D1,Standard_D2,Standard_D3,Standard_D4,Standard_D11,Standard_D12,Standard_D13,Standard_D14,Standard_NV6,Standard_NV12,Standard_NV24,Standard_NV6_Promo,Standard_NV12_Promo,Standard_NV24_Promo,Standard_NC4as_T4_v3,Standard_NC8as_T4_v3,Standard_NC16as_T4_v3,Standard_NC64as_T4_v3,Standard_NV6s_v2,Standard_NV12s_v2,Standard_NV24s_v2,Standard_NV12s_v3,Standard_NV24s_v3,Standard_NV48s_v3,Standard_HB120rs_v2,Standard_D2ds_v4,Standard_D4ds_v4,Standard_D8ds_v4,Standard_D16ds_v4,Standard_D32ds_v4,Standard_D48ds_v4,Standard_D64ds_v4,Standard_D2ds_v5,Standard_D4ds_v5,Standard_D8ds_v5,Standard_D16ds_v5,Standard_D32ds_v5,Standard_D48ds_v5,Standard_D64ds_v5,Standard_D96ds_v5,Standard_D2d_v4,Standard_D4d_v4,Standard_D8d_v4,Standard_D16d_v4,Standard_D32d_v4,Standard_D48d_v4,Standard_D64d_v4,Standard_D2d_v5,Standard_D4d_v5,Standard_D8d_v5,Standard_D16d_v5,Standard_D32d_v5,Standard_D48d_v5,Standard_D64d_v5,Standard_D96d_v5,Standard_D2s_v4,Standard_D4s_v4,Standard_D8s_v4,Standard_D16s_v4,Standard_D32s_v4,Standard_D48s_v4,Standard_D64s_v4,Standard_D2s_v5,Standard_D4s_v5,Standard_D8s_v5,Standard_D16s_v5,Standard_D32s_v5,Standard_D48s_v5,Standard_D64s_v5,Standard_D96s_v5,Standard_D2_v4,Standard_D4_v4,Standard_D8_v4,Standard_D16_v4,Standard_D32_v4,Standard_D48_v4,Standard_D64_v4,Standard_D2_v5,Standard_D4_v5,Standard_D8_v5,Standard_D16_v5,Standard_D32_v5,Standard_D48_v5,Standard_D64_v5,Standard_D96_v5,Standard_E2ds_v4,Standard_E4-2ds_v4,Standard_E4ds_v4,Standard_E8-2ds_v4,Standard_E8-4ds_v4,Standard_E8ds_v4,Standard_E16-4ds_v4,Standard_E16-8ds_v4,Standard_E16ds_v4,Standard_E20ds_v4,Standard_E32-8ds_v4,Standard_E32-16ds_v4,Standard_E32ds_v4,Standard_E48ds_v4,Standard_E64-16ds_v4,Standard_E64-32ds_v4,Standard_E64ds_v4,Standard_E80ids_v4,Standard_E2ds_v5,Standard_E4-2ds_v5,Standard_E4ds_v5,Standard_E8-2ds_v5,Standard_E8-4ds_v5,Standard_E8ds_v5,Standard_E16-4ds_v5,Standard_E16-8ds_v5,Standard_E16ds_v5,Standard_E20ds_v5,Standard_E32-8ds_v5,Standard_E32-16ds_v5,Standard_E32ds_v5,Standard_E48ds_v5,Standard_E64-16ds_v5,Standard_E64-32ds_v5,Standard_E64ds_v5,Standard_E96-24ds_v5,Standard_E96-48ds_v5,Standard_E96ds_v5,Standard_E104ids_v5,Standard_E2d_v4,Standard_E4d_v4,Standard_E8d_v4,Standard_E16d_v4,Standard_E20d_v4,Standard_E32d_v4,Standard_E48d_v4,Standard_E64d_v4,Standard_E2d_v5,Standard_E4d_v5,Standard_E8d_v5,Standard_E16d_v5,Standard_E20d_v5,Standard_E32d_v5,Standard_E48d_v5,Standard_E64d_v5,Standard_E96d_v5,Standard_E104id_v5,Standard_E2s_v4,Standard_E4-2s_v4,Standard_E4s_v4,Standard_E8-2s_v4,Standard_E8-4s_v4,Standard_E8s_v4,Standard_E16-4s_v4,Standard_E16-8s_v4,Standard_E16s_v4,Standard_E20s_v4,Standard_E32-8s_v4,Standard_E32-16s_v4,Standard_E32s_v4,Standard_E48s_v4,Standard_E64-16s_v4,Standard_E64-32s_v4,Standard_E64s_v4,Standard_E80is_v4,Standard_E2s_v5,Standard_E4-2s_v5,Standard_E4s_v5,Standard_E8-2s_v5,Standard_E8-4s_v5,Standard_E8s_v5,Standard_E16-4s_v5,Standard_E16-8s_v5,Standard_E16s_v5,Standard_E20s_v5,Standard_E32-8s_v5,Standard_E32-16s_v5,Standard_E32s_v5,Standard_E48s_v5,Standard_E64-16s_v5,Standard_E64-32s_v5,Standard_E64s_v5,Standard_E96-24s_v5,Standard_E96-48s_v5,Standard_E96s_v5,Standard_E104is_v5,Standard_E2_v4,Standard_E4_v4,Standard_E8_v4,Standard_E16_v4,Standard_E20_v4,Standard_E32_v4,Standard_E48_v4,Standard_E64_v4,Standard_E2_v5,Standard_E4_v5,Standard_E8_v5,Standard_E16_v5,Standard_E20_v5,Standard_E32_v5,Standard_E48_v5,Standard_E64_v5,Standard_E96_v5,Standard_E104i_v5,Standard_F2s_v2,Standard_F4s_v2,Standard_F8s_v2,Standard_F16s_v2,Standard_F32s_v2,Standard_F48s_v2,Standard_F64s_v2,Standard_F72s_v2,Standard_NC6s_v2,Standard_NC12s_v2,Standard_NC24rs_v2,Standard_NC24s_v2,Standard_NC6,Standard_NC12,Standard_NC24,Standard_NC24r,Standard_NC6_Promo,Standard_NC12_Promo,Standard_NC24_Promo,Standard_NC24r_Promo,Standard_DS1,Standard_DS2,Standard_DS3,Standard_DS4,Standard_DS11,Standard_DS12,Standard_DS13,Standard_DS14,Standard_L8s_v2,Standard_L16s_v2,Standard_L32s_v2,Standard_L48s_v2,Standard_L64s_v2,Standard_L80s_v2,Standard_M64,Standard_M64m,Standard_M128,Standard_M128m,Standard_M8-2ms,Standard_M8-4ms,Standard_M8ms,Standard_M16-4ms,Standard_M16-8ms,Standard_M16ms,Standard_M32-8ms,Standard_M32-16ms,Standard_M32ls,Standard_M32ms,Standard_M32ts,Standard_M64-16ms,Standard_M64-32ms,Standard_M64ls,Standard_M64ms,Standard_M64s,Standard_M128-32ms,Standard_M128-64ms,Standard_M128ms,Standard_M128s,Standard_M32ms_v2,Standard_M64ms_v2,Standard_M64s_v2,Standard_M128ms_v2,Standard_M128s_v2,Standard_M192ims_v2,Standard_M192is_v2,Standard_M32dms_v2,Standard_M64dms_v2,Standard_M64ds_v2,Standard_M128dms_v2,Standard_M128ds_v2,Standard_M192idms_v2,Standard_M192ids_v2,Standard_DC8_v2,Standard_DC1s_v2,Standard_DC2s_v2,Standard_DC4s_v2,Standard_ND40rs_v2,Standard_FX4mds,Standard_FX12mds,Standard_FX24mds,Standard_FX36mds,Standard_FX48mds,Standard_NP10s,Standard_NP20s,Standard_NP40s,Standard_D2as_v5,Standard_D4as_v5,Standard_D8as_v5,Standard_D16as_v5,Standard_D32as_v5,Standard_D48as_v5,Standard_D64as_v5,Standard_D96as_v5,Standard_E2as_v5,Standard_E4-2as_v5,Standard_E4as_v5,Standard_E8-2as_v5,Standard_E8-4as_v5,Standard_E8as_v5,Standard_E16-4as_v5,Standard_E16-8as_v5,Standard_E16as_v5,Standard_E20as_v5,Standard_E32-8as_v5,Standard_E32-16as_v5,Standard_E32as_v5,Standard_E48as_v5,Standard_E64-16as_v5,Standard_E64-32as_v5,Standard_E64as_v5,Standard_E96-24as_v5,Standard_E96-48as_v5,Standard_E96as_v5,Standard_D2ads_v5,Standard_D4ads_v5,Standard_D8ads_v5,Standard_D16ads_v5,Standard_D32ads_v5,Standard_D48ads_v5,Standard_D64ads_v5,Standard_D96ads_v5,Standard_E2ads_v5,Standard_E4-2ads_v5,Standard_E4ads_v5,Standard_E8-2ads_v5,Standard_E8-4ads_v5,Standard_E8ads_v5,Standard_E16-4ads_v5,Standard_E16-8ads_v5,Standard_E16ads_v5,Standard_E20ads_v5,Standard_E32-8ads_v5,Standard_E32-16ads_v5,Standard_E32ads_v5,Standard_E48ads_v5,Standard_E64-16ads_v5,Standard_E64-32ads_v5,Standard_E64ads_v5,Standard_E96-24ads_v5,Standard_E96-48ads_v5,Standard_E96ads_v5,Standard_HC44rs,Standard_ND6s,Standard_ND12s,Standard_ND24rs,Standard_ND24s,Standard_DC2s,Standard_DC4s,Standard_HB120-16rs_v3,Standard_HB120-32rs_v3,Standard_HB120-64rs_v3,Standard_HB120-96rs_v3,Standard_HB120rs_v3,Standard_NV4as_v4,Standard_NV8as_v4,Standard_NV16as_v4,Standard_NV32as_v4,Standard_NC6s_v3,Standard_NC12s_v3,Standard_NC24rs_v3,Standard_NC24s_v3,Standard_PB6s,Standard_HB60rs,Standard_ND96asr_v4,Standard_ND40s_v3. Find out more on the valid VM sizes in each region at https://aka.ms/azure-regions.
Target: vmSize
yetunde@Azure:~$ az vm resize --resource-group ytarg --name webserver --size Standard_DS1_v2.name
(InvalidParameter) The value Standard_DS1_v2.name provided for the VM size is not valid. The valid sizes in the current region are: Standard_B1ls,Standard_B1ms,Standard_B1s,Standard_B2ms,Standard_B2s,Standard_B4ms,Standard_B8ms,Standard_B12ms,Standard_B16ms,Standard_B20ms,Standard_DS1_v2,Standard_DS2_v2,Standard_DS3_v2,Standard_DS4_v2,Standard_DS5_v2,Standard_DS11-1_v2,Standard_DS11_v2,Standard_DS12-1_v2,Standard_DS12-2_v2,Standard_DS12_v2,Standard_DS13-2_v2,Standard_DS13-4_v2,Standard_DS13_v2,Standard_DS14-4_v2,Standard_DS14-8_v2,Standard_DS14_v2,Standard_DS15_v2,Standard_DS2_v2_Promo,Standard_DS3_v2_Promo,Standard_DS4_v2_Promo,Standard_DS5_v2_Promo,Standard_DS11_v2_Promo,Standard_DS12_v2_Promo,Standard_DS13_v2_Promo,Standard_DS14_v2_Promo,Standard_F1s,Standard_F2s,Standard_F4s,Standard_F8s,Standard_F16s,Standard_D2s_v3,Standard_D4s_v3,Standard_D8s_v3,Standard_D16s_v3,Standard_D32s_v3,Standard_D2a_v4,Standard_D4a_v4,Standard_D8a_v4,Standard_D16a_v4,Standard_D32a_v4,Standard_D48a_v4,Standard_D64a_v4,Standard_D96a_v4,Standard_D2as_v4,Standard_D4as_v4,Standard_D8as_v4,Standard_D16as_v4,Standard_D32as_v4,Standard_D48as_v4,Standard_D64as_v4,Standard_D96as_v4,Standard_E2a_v4,Standard_E4a_v4,Standard_E8a_v4,Standard_E16a_v4,Standard_E20a_v4,Standard_E32a_v4,Standard_E48a_v4,Standard_E64a_v4,Standard_E96a_v4,Standard_E2as_v4,Standard_E4-2as_v4,Standard_E4as_v4,Standard_E8-2as_v4,Standard_E8-4as_v4,Standard_E8as_v4,Standard_E16-4as_v4,Standard_E16-8as_v4,Standard_E16as_v4,Standard_E20as_v4,Standard_E32-8as_v4,Standard_E32-16as_v4,Standard_E32as_v4,Standard_E48as_v4,Standard_E64-16as_v4,Standard_E64-32as_v4,Standard_E64as_v4,Standard_E96-24as_v4,Standard_E96-48as_v4,Standard_E96as_v4,Standard_D1_v2,Standard_D2_v2,Standard_D3_v2,Standard_D4_v2,Standard_D5_v2,Standard_D11_v2,Standard_D12_v2,Standard_D13_v2,Standard_D14_v2,Standard_D15_v2,Standard_D2_v2_Promo,Standard_D3_v2_Promo,Standard_D4_v2_Promo,Standard_D5_v2_Promo,Standard_D11_v2_Promo,Standard_D12_v2_Promo,Standard_D13_v2_Promo,Standard_D14_v2_Promo,Standard_F1,Standard_F2,Standard_F4,Standard_F8,Standard_F16,Standard_A1_v2,Standard_A2m_v2,Standard_A2_v2,Standard_A4m_v2,Standard_A4_v2,Standard_A8m_v2,Standard_A8_v2,Standard_D2_v3,Standard_D4_v3,Standard_D8_v3,Standard_D16_v3,Standard_D32_v3,Standard_D48_v3,Standard_D64_v3,Standard_D48s_v3,Standard_D64s_v3,Standard_E2_v3,Standard_E4_v3,Standard_E8_v3,Standard_E16_v3,Standard_E20_v3,Standard_E32_v3,Standard_E48_v3,Standard_E64_v3,Standard_E2s_v3,Standard_E4-2s_v3,Standard_E4s_v3,Standard_E8-2s_v3,Standard_E8-4s_v3,Standard_E8s_v3,Standard_E16-4s_v3,Standard_E16-8s_v3,Standard_E16s_v3,Standard_E20s_v3,Standard_E32-8s_v3,Standard_E32-16s_v3,Standard_E32s_v3,Standard_E48s_v3,Standard_E64-16s_v3,Standard_E64-32s_v3,Standard_E64s_v3,Standard_A0,Standard_A1,Standard_A2,Standard_A3,Standard_A5,Standard_A4,Standard_A6,Standard_A7,Basic_A0,Basic_A1,Basic_A2,Basic_A3,Basic_A4,Standard_E64i_v3,Standard_E64is_v3,Standard_M208ms_v2,Standard_M208s_v2,Standard_M416-208s_v2,Standard_M416s_v2,Standard_M416-208ms_v2,Standard_M416ms_v2,Standard_H8,Standard_H8_Promo,Standard_H16,Standard_H16_Promo,Standard_H8m,Standard_H8m_Promo,Standard_H16m,Standard_H16m_Promo,Standard_H16r,Standard_H16r_Promo,Standard_H16mr,Standard_H16mr_Promo,Standard_D1,Standard_D2,Standard_D3,Standard_D4,Standard_D11,Standard_D12,Standard_D13,Standard_D14,Standard_NV6,Standard_NV12,Standard_NV24,Standard_NV6_Promo,Standard_NV12_Promo,Standard_NV24_Promo,Standard_NC4as_T4_v3,Standard_NC8as_T4_v3,Standard_NC16as_T4_v3,Standard_NC64as_T4_v3,Standard_NV6s_v2,Standard_NV12s_v2,Standard_NV24s_v2,Standard_NV12s_v3,Standard_NV24s_v3,Standard_NV48s_v3,Standard_HB120rs_v2,Standard_D2ds_v4,Standard_D4ds_v4,Standard_D8ds_v4,Standard_D16ds_v4,Standard_D32ds_v4,Standard_D48ds_v4,Standard_D64ds_v4,Standard_D2ds_v5,Standard_D4ds_v5,Standard_D8ds_v5,Standard_D16ds_v5,Standard_D32ds_v5,Standard_D48ds_v5,Standard_D64ds_v5,Standard_D96ds_v5,Standard_D2d_v4,Standard_D4d_v4,Standard_D8d_v4,Standard_D16d_v4,Standard_D32d_v4,Standard_D48d_v4,Standard_D64d_v4,Standard_D2d_v5,Standard_D4d_v5,Standard_D8d_v5,Standard_D16d_v5,Standard_D32d_v5,Standard_D48d_v5,Standard_D64d_v5,Standard_D96d_v5,Standard_D2s_v4,Standard_D4s_v4,Standard_D8s_v4,Standard_D16s_v4,Standard_D32s_v4,Standard_D48s_v4,Standard_D64s_v4,Standard_D2s_v5,Standard_D4s_v5,Standard_D8s_v5,Standard_D16s_v5,Standard_D32s_v5,Standard_D48s_v5,Standard_D64s_v5,Standard_D96s_v5,Standard_D2_v4,Standard_D4_v4,Standard_D8_v4,Standard_D16_v4,Standard_D32_v4,Standard_D48_v4,Standard_D64_v4,Standard_D2_v5,Standard_D4_v5,Standard_D8_v5,Standard_D16_v5,Standard_D32_v5,Standard_D48_v5,Standard_D64_v5,Standard_D96_v5,Standard_E2ds_v4,Standard_E4-2ds_v4,Standard_E4ds_v4,Standard_E8-2ds_v4,Standard_E8-4ds_v4,Standard_E8ds_v4,Standard_E16-4ds_v4,Standard_E16-8ds_v4,Standard_E16ds_v4,Standard_E20ds_v4,Standard_E32-8ds_v4,Standard_E32-16ds_v4,Standard_E32ds_v4,Standard_E48ds_v4,Standard_E64-16ds_v4,Standard_E64-32ds_v4,Standard_E64ds_v4,Standard_E80ids_v4,Standard_E2ds_v5,Standard_E4-2ds_v5,Standard_E4ds_v5,Standard_E8-2ds_v5,Standard_E8-4ds_v5,Standard_E8ds_v5,Standard_E16-4ds_v5,Standard_E16-8ds_v5,Standard_E16ds_v5,Standard_E20ds_v5,Standard_E32-8ds_v5,Standard_E32-16ds_v5,Standard_E32ds_v5,Standard_E48ds_v5,Standard_E64-16ds_v5,Standard_E64-32ds_v5,Standard_E64ds_v5,Standard_E96-24ds_v5,Standard_E96-48ds_v5,Standard_E96ds_v5,Standard_E104ids_v5,Standard_E2d_v4,Standard_E4d_v4,Standard_E8d_v4,Standard_E16d_v4,Standard_E20d_v4,Standard_E32d_v4,Standard_E48d_v4,Standard_E64d_v4,Standard_E2d_v5,Standard_E4d_v5,Standard_E8d_v5,Standard_E16d_v5,Standard_E20d_v5,Standard_E32d_v5,Standard_E48d_v5,Standard_E64d_v5,Standard_E96d_v5,Standard_E104id_v5,Standard_E2s_v4,Standard_E4-2s_v4,Standard_E4s_v4,Standard_E8-2s_v4,Standard_E8-4s_v4,Standard_E8s_v4,Standard_E16-4s_v4,Standard_E16-8s_v4,Standard_E16s_v4,Standard_E20s_v4,Standard_E32-8s_v4,Standard_E32-16s_v4,Standard_E32s_v4,Standard_E48s_v4,Standard_E64-16s_v4,Standard_E64-32s_v4,Standard_E64s_v4,Standard_E80is_v4,Standard_E2s_v5,Standard_E4-2s_v5,Standard_E4s_v5,Standard_E8-2s_v5,Standard_E8-4s_v5,Standard_E8s_v5,Standard_E16-4s_v5,Standard_E16-8s_v5,Standard_E16s_v5,Standard_E20s_v5,Standard_E32-8s_v5,Standard_E32-16s_v5,Standard_E32s_v5,Standard_E48s_v5,Standard_E64-16s_v5,Standard_E64-32s_v5,Standard_E64s_v5,Standard_E96-24s_v5,Standard_E96-48s_v5,Standard_E96s_v5,Standard_E104is_v5,Standard_E2_v4,Standard_E4_v4,Standard_E8_v4,Standard_E16_v4,Standard_E20_v4,Standard_E32_v4,Standard_E48_v4,Standard_E64_v4,Standard_E2_v5,Standard_E4_v5,Standard_E8_v5,Standard_E16_v5,Standard_E20_v5,Standard_E32_v5,Standard_E48_v5,Standard_E64_v5,Standard_E96_v5,Standard_E104i_v5,Standard_F2s_v2,Standard_F4s_v2,Standard_F8s_v2,Standard_F16s_v2,Standard_F32s_v2,Standard_F48s_v2,Standard_F64s_v2,Standard_F72s_v2,Standard_NC6s_v2,Standard_NC12s_v2,Standard_NC24rs_v2,Standard_NC24s_v2,Standard_NC6,Standard_NC12,Standard_NC24,Standard_NC24r,Standard_NC6_Promo,Standard_NC12_Promo,Standard_NC24_Promo,Standard_NC24r_Promo,Standard_DS1,Standard_DS2,Standard_DS3,Standard_DS4,Standard_DS11,Standard_DS12,Standard_DS13,Standard_DS14,Standard_L8s_v2,Standard_L16s_v2,Standard_L32s_v2,Standard_L48s_v2,Standard_L64s_v2,Standard_L80s_v2,Standard_M64,Standard_M64m,Standard_M128,Standard_M128m,Standard_M8-2ms,Standard_M8-4ms,Standard_M8ms,Standard_M16-4ms,Standard_M16-8ms,Standard_M16ms,Standard_M32-8ms,Standard_M32-16ms,Standard_M32ls,Standard_M32ms,Standard_M32ts,Standard_M64-16ms,Standard_M64-32ms,Standard_M64ls,Standard_M64ms,Standard_M64s,Standard_M128-32ms,Standard_M128-64ms,Standard_M128ms,Standard_M128s,Standard_M32ms_v2,Standard_M64ms_v2,Standard_M64s_v2,Standard_M128ms_v2,Standard_M128s_v2,Standard_M192ims_v2,Standard_M192is_v2,Standard_M32dms_v2,Standard_M64dms_v2,Standard_M64ds_v2,Standard_M128dms_v2,Standard_M128ds_v2,Standard_M192idms_v2,Standard_M192ids_v2,Standard_DC8_v2,Standard_DC1s_v2,Standard_DC2s_v2,Standard_DC4s_v2,Standard_ND40rs_v2,Standard_FX4mds,Standard_FX12mds,Standard_FX24mds,Standard_FX36mds,Standard_FX48mds,Standard_NP10s,Standard_NP20s,Standard_NP40s,Standard_D2as_v5,Standard_D4as_v5,Standard_D8as_v5,Standard_D16as_v5,Standard_D32as_v5,Standard_D48as_v5,Standard_D64as_v5,Standard_D96as_v5,Standard_E2as_v5,Standard_E4-2as_v5,Standard_E4as_v5,Standard_E8-2as_v5,Standard_E8-4as_v5,Standard_E8as_v5,Standard_E16-4as_v5,Standard_E16-8as_v5,Standard_E16as_v5,Standard_E20as_v5,Standard_E32-8as_v5,Standard_E32-16as_v5,Standard_E32as_v5,Standard_E48as_v5,Standard_E64-16as_v5,Standard_E64-32as_v5,Standard_E64as_v5,Standard_E96-24as_v5,Standard_E96-48as_v5,Standard_E96as_v5,Standard_D2ads_v5,Standard_D4ads_v5,Standard_D8ads_v5,Standard_D16ads_v5,Standard_D32ads_v5,Standard_D48ads_v5,Standard_D64ads_v5,Standard_D96ads_v5,Standard_E2ads_v5,Standard_E4-2ads_v5,Standard_E4ads_v5,Standard_E8-2ads_v5,Standard_E8-4ads_v5,Standard_E8ads_v5,Standard_E16-4ads_v5,Standard_E16-8ads_v5,Standard_E16ads_v5,Standard_E20ads_v5,Standard_E32-8ads_v5,Standard_E32-16ads_v5,Standard_E32ads_v5,Standard_E48ads_v5,Standard_E64-16ads_v5,Standard_E64-32ads_v5,Standard_E64ads_v5,Standard_E96-24ads_v5,Standard_E96-48ads_v5,Standard_E96ads_v5,Standard_HC44rs,Standard_ND6s,Standard_ND12s,Standard_ND24rs,Standard_ND24s,Standard_DC2s,Standard_DC4s,Standard_HB120-16rs_v3,Standard_HB120-32rs_v3,Standard_HB120-64rs_v3,Standard_HB120-96rs_v3,Standard_HB120rs_v3,Standard_NV4as_v4,Standard_NV8as_v4,Standard_NV16as_v4,Standard_NV32as_v4,Standard_NC6s_v3,Standard_NC12s_v3,Standard_NC24rs_v3,Standard_NC24s_v3,Standard_PB6s,Standard_HB60rs,Standard_ND96asr_v4,Standard_ND40s_v3. Find out more on the valid VM sizes in each region at https://aka.ms/azure-regions.
Code: InvalidParameter
Message: The value Standard_DS1_v2.name provided for the VM size is not valid. The valid sizes in the current region are: Standard_B1ls,Standard_B1ms,Standard_B1s,Standard_B2ms,Standard_B2s,Standard_B4ms,Standard_B8ms,Standard_B12ms,Standard_B16ms,Standard_B20ms,Standard_DS1_v2,Standard_DS2_v2,Standard_DS3_v2,Standard_DS4_v2,Standard_DS5_v2,Standard_DS11-1_v2,Standard_DS11_v2,Standard_DS12-1_v2,Standard_DS12-2_v2,Standard_DS12_v2,Standard_DS13-2_v2,Standard_DS13-4_v2,Standard_DS13_v2,Standard_DS14-4_v2,Standard_DS14-8_v2,Standard_DS14_v2,Standard_DS15_v2,Standard_DS2_v2_Promo,Standard_DS3_v2_Promo,Standard_DS4_v2_Promo,Standard_DS5_v2_Promo,Standard_DS11_v2_Promo,Standard_DS12_v2_Promo,Standard_DS13_v2_Promo,Standard_DS14_v2_Promo,Standard_F1s,Standard_F2s,Standard_F4s,Standard_F8s,Standard_F16s,Standard_D2s_v3,Standard_D4s_v3,Standard_D8s_v3,Standard_D16s_v3,Standard_D32s_v3,Standard_D2a_v4,Standard_D4a_v4,Standard_D8a_v4,Standard_D16a_v4,Standard_D32a_v4,Standard_D48a_v4,Standard_D64a_v4,Standard_D96a_v4,Standard_D2as_v4,Standard_D4as_v4,Standard_D8as_v4,Standard_D16as_v4,Standard_D32as_v4,Standard_D48as_v4,Standard_D64as_v4,Standard_D96as_v4,Standard_E2a_v4,Standard_E4a_v4,Standard_E8a_v4,Standard_E16a_v4,Standard_E20a_v4,Standard_E32a_v4,Standard_E48a_v4,Standard_E64a_v4,Standard_E96a_v4,Standard_E2as_v4,Standard_E4-2as_v4,Standard_E4as_v4,Standard_E8-2as_v4,Standard_E8-4as_v4,Standard_E8as_v4,Standard_E16-4as_v4,Standard_E16-8as_v4,Standard_E16as_v4,Standard_E20as_v4,Standard_E32-8as_v4,Standard_E32-16as_v4,Standard_E32as_v4,Standard_E48as_v4,Standard_E64-16as_v4,Standard_E64-32as_v4,Standard_E64as_v4,Standard_E96-24as_v4,Standard_E96-48as_v4,Standard_E96as_v4,Standard_D1_v2,Standard_D2_v2,Standard_D3_v2,Standard_D4_v2,Standard_D5_v2,Standard_D11_v2,Standard_D12_v2,Standard_D13_v2,Standard_D14_v2,Standard_D15_v2,Standard_D2_v2_Promo,Standard_D3_v2_Promo,Standard_D4_v2_Promo,Standard_D5_v2_Promo,Standard_D11_v2_Promo,Standard_D12_v2_Promo,Standard_D13_v2_Promo,Standard_D14_v2_Promo,Standard_F1,Standard_F2,Standard_F4,Standard_F8,Standard_F16,Standard_A1_v2,Standard_A2m_v2,Standard_A2_v2,Standard_A4m_v2,Standard_A4_v2,Standard_A8m_v2,Standard_A8_v2,Standard_D2_v3,Standard_D4_v3,Standard_D8_v3,Standard_D16_v3,Standard_D32_v3,Standard_D48_v3,Standard_D64_v3,Standard_D48s_v3,Standard_D64s_v3,Standard_E2_v3,Standard_E4_v3,Standard_E8_v3,Standard_E16_v3,Standard_E20_v3,Standard_E32_v3,Standard_E48_v3,Standard_E64_v3,Standard_E2s_v3,Standard_E4-2s_v3,Standard_E4s_v3,Standard_E8-2s_v3,Standard_E8-4s_v3,Standard_E8s_v3,Standard_E16-4s_v3,Standard_E16-8s_v3,Standard_E16s_v3,Standard_E20s_v3,Standard_E32-8s_v3,Standard_E32-16s_v3,Standard_E32s_v3,Standard_E48s_v3,Standard_E64-16s_v3,Standard_E64-32s_v3,Standard_E64s_v3,Standard_A0,Standard_A1,Standard_A2,Standard_A3,Standard_A5,Standard_A4,Standard_A6,Standard_A7,Basic_A0,Basic_A1,Basic_A2,Basic_A3,Basic_A4,Standard_E64i_v3,Standard_E64is_v3,Standard_M208ms_v2,Standard_M208s_v2,Standard_M416-208s_v2,Standard_M416s_v2,Standard_M416-208ms_v2,Standard_M416ms_v2,Standard_H8,Standard_H8_Promo,Standard_H16,Standard_H16_Promo,Standard_H8m,Standard_H8m_Promo,Standard_H16m,Standard_H16m_Promo,Standard_H16r,Standard_H16r_Promo,Standard_H16mr,Standard_H16mr_Promo,Standard_D1,Standard_D2,Standard_D3,Standard_D4,Standard_D11,Standard_D12,Standard_D13,Standard_D14,Standard_NV6,Standard_NV12,Standard_NV24,Standard_NV6_Promo,Standard_NV12_Promo,Standard_NV24_Promo,Standard_NC4as_T4_v3,Standard_NC8as_T4_v3,Standard_NC16as_T4_v3,Standard_NC64as_T4_v3,Standard_NV6s_v2,Standard_NV12s_v2,Standard_NV24s_v2,Standard_NV12s_v3,Standard_NV24s_v3,Standard_NV48s_v3,Standard_HB120rs_v2,Standard_D2ds_v4,Standard_D4ds_v4,Standard_D8ds_v4,Standard_D16ds_v4,Standard_D32ds_v4,Standard_D48ds_v4,Standard_D64ds_v4,Standard_D2ds_v5,Standard_D4ds_v5,Standard_D8ds_v5,Standard_D16ds_v5,Standard_D32ds_v5,Standard_D48ds_v5,Standard_D64ds_v5,Standard_D96ds_v5,Standard_D2d_v4,Standard_D4d_v4,Standard_D8d_v4,Standard_D16d_v4,Standard_D32d_v4,Standard_D48d_v4,Standard_D64d_v4,Standard_D2d_v5,Standard_D4d_v5,Standard_D8d_v5,Standard_D16d_v5,Standard_D32d_v5,Standard_D48d_v5,Standard_D64d_v5,Standard_D96d_v5,Standard_D2s_v4,Standard_D4s_v4,Standard_D8s_v4,Standard_D16s_v4,Standard_D32s_v4,Standard_D48s_v4,Standard_D64s_v4,Standard_D2s_v5,Standard_D4s_v5,Standard_D8s_v5,Standard_D16s_v5,Standard_D32s_v5,Standard_D48s_v5,Standard_D64s_v5,Standard_D96s_v5,Standard_D2_v4,Standard_D4_v4,Standard_D8_v4,Standard_D16_v4,Standard_D32_v4,Standard_D48_v4,Standard_D64_v4,Standard_D2_v5,Standard_D4_v5,Standard_D8_v5,Standard_D16_v5,Standard_D32_v5,Standard_D48_v5,Standard_D64_v5,Standard_D96_v5,Standard_E2ds_v4,Standard_E4-2ds_v4,Standard_E4ds_v4,Standard_E8-2ds_v4,Standard_E8-4ds_v4,Standard_E8ds_v4,Standard_E16-4ds_v4,Standard_E16-8ds_v4,Standard_E16ds_v4,Standard_E20ds_v4,Standard_E32-8ds_v4,Standard_E32-16ds_v4,Standard_E32ds_v4,Standard_E48ds_v4,Standard_E64-16ds_v4,Standard_E64-32ds_v4,Standard_E64ds_v4,Standard_E80ids_v4,Standard_E2ds_v5,Standard_E4-2ds_v5,Standard_E4ds_v5,Standard_E8-2ds_v5,Standard_E8-4ds_v5,Standard_E8ds_v5,Standard_E16-4ds_v5,Standard_E16-8ds_v5,Standard_E16ds_v5,Standard_E20ds_v5,Standard_E32-8ds_v5,Standard_E32-16ds_v5,Standard_E32ds_v5,Standard_E48ds_v5,Standard_E64-16ds_v5,Standard_E64-32ds_v5,Standard_E64ds_v5,Standard_E96-24ds_v5,Standard_E96-48ds_v5,Standard_E96ds_v5,Standard_E104ids_v5,Standard_E2d_v4,Standard_E4d_v4,Standard_E8d_v4,Standard_E16d_v4,Standard_E20d_v4,Standard_E32d_v4,Standard_E48d_v4,Standard_E64d_v4,Standard_E2d_v5,Standard_E4d_v5,Standard_E8d_v5,Standard_E16d_v5,Standard_E20d_v5,Standard_E32d_v5,Standard_E48d_v5,Standard_E64d_v5,Standard_E96d_v5,Standard_E104id_v5,Standard_E2s_v4,Standard_E4-2s_v4,Standard_E4s_v4,Standard_E8-2s_v4,Standard_E8-4s_v4,Standard_E8s_v4,Standard_E16-4s_v4,Standard_E16-8s_v4,Standard_E16s_v4,Standard_E20s_v4,Standard_E32-8s_v4,Standard_E32-16s_v4,Standard_E32s_v4,Standard_E48s_v4,Standard_E64-16s_v4,Standard_E64-32s_v4,Standard_E64s_v4,Standard_E80is_v4,Standard_E2s_v5,Standard_E4-2s_v5,Standard_E4s_v5,Standard_E8-2s_v5,Standard_E8-4s_v5,Standard_E8s_v5,Standard_E16-4s_v5,Standard_E16-8s_v5,Standard_E16s_v5,Standard_E20s_v5,Standard_E32-8s_v5,Standard_E32-16s_v5,Standard_E32s_v5,Standard_E48s_v5,Standard_E64-16s_v5,Standard_E64-32s_v5,Standard_E64s_v5,Standard_E96-24s_v5,Standard_E96-48s_v5,Standard_E96s_v5,Standard_E104is_v5,Standard_E2_v4,Standard_E4_v4,Standard_E8_v4,Standard_E16_v4,Standard_E20_v4,Standard_E32_v4,Standard_E48_v4,Standard_E64_v4,Standard_E2_v5,Standard_E4_v5,Standard_E8_v5,Standard_E16_v5,Standard_E20_v5,Standard_E32_v5,Standard_E48_v5,Standard_E64_v5,Standard_E96_v5,Standard_E104i_v5,Standard_F2s_v2,Standard_F4s_v2,Standard_F8s_v2,Standard_F16s_v2,Standard_F32s_v2,Standard_F48s_v2,Standard_F64s_v2,Standard_F72s_v2,Standard_NC6s_v2,Standard_NC12s_v2,Standard_NC24rs_v2,Standard_NC24s_v2,Standard_NC6,Standard_NC12,Standard_NC24,Standard_NC24r,Standard_NC6_Promo,Standard_NC12_Promo,Standard_NC24_Promo,Standard_NC24r_Promo,Standard_DS1,Standard_DS2,Standard_DS3,Standard_DS4,Standard_DS11,Standard_DS12,Standard_DS13,Standard_DS14,Standard_L8s_v2,Standard_L16s_v2,Standard_L32s_v2,Standard_L48s_v2,Standard_L64s_v2,Standard_L80s_v2,Standard_M64,Standard_M64m,Standard_M128,Standard_M128m,Standard_M8-2ms,Standard_M8-4ms,Standard_M8ms,Standard_M16-4ms,Standard_M16-8ms,Standard_M16ms,Standard_M32-8ms,Standard_M32-16ms,Standard_M32ls,Standard_M32ms,Standard_M32ts,Standard_M64-16ms,Standard_M64-32ms,Standard_M64ls,Standard_M64ms,Standard_M64s,Standard_M128-32ms,Standard_M128-64ms,Standard_M128ms,Standard_M128s,Standard_M32ms_v2,Standard_M64ms_v2,Standard_M64s_v2,Standard_M128ms_v2,Standard_M128s_v2,Standard_M192ims_v2,Standard_M192is_v2,Standard_M32dms_v2,Standard_M64dms_v2,Standard_M64ds_v2,Standard_M128dms_v2,Standard_M128ds_v2,Standard_M192idms_v2,Standard_M192ids_v2,Standard_DC8_v2,Standard_DC1s_v2,Standard_DC2s_v2,Standard_DC4s_v2,Standard_ND40rs_v2,Standard_FX4mds,Standard_FX12mds,Standard_FX24mds,Standard_FX36mds,Standard_FX48mds,Standard_NP10s,Standard_NP20s,Standard_NP40s,Standard_D2as_v5,Standard_D4as_v5,Standard_D8as_v5,Standard_D16as_v5,Standard_D32as_v5,Standard_D48as_v5,Standard_D64as_v5,Standard_D96as_v5,Standard_E2as_v5,Standard_E4-2as_v5,Standard_E4as_v5,Standard_E8-2as_v5,Standard_E8-4as_v5,Standard_E8as_v5,Standard_E16-4as_v5,Standard_E16-8as_v5,Standard_E16as_v5,Standard_E20as_v5,Standard_E32-8as_v5,Standard_E32-16as_v5,Standard_E32as_v5,Standard_E48as_v5,Standard_E64-16as_v5,Standard_E64-32as_v5,Standard_E64as_v5,Standard_E96-24as_v5,Standard_E96-48as_v5,Standard_E96as_v5,Standard_D2ads_v5,Standard_D4ads_v5,Standard_D8ads_v5,Standard_D16ads_v5,Standard_D32ads_v5,Standard_D48ads_v5,Standard_D64ads_v5,Standard_D96ads_v5,Standard_E2ads_v5,Standard_E4-2ads_v5,Standard_E4ads_v5,Standard_E8-2ads_v5,Standard_E8-4ads_v5,Standard_E8ads_v5,Standard_E16-4ads_v5,Standard_E16-8ads_v5,Standard_E16ads_v5,Standard_E20ads_v5,Standard_E32-8ads_v5,Standard_E32-16ads_v5,Standard_E32ads_v5,Standard_E48ads_v5,Standard_E64-16ads_v5,Standard_E64-32ads_v5,Standard_E64ads_v5,Standard_E96-24ads_v5,Standard_E96-48ads_v5,Standard_E96ads_v5,Standard_HC44rs,Standard_ND6s,Standard_ND12s,Standard_ND24rs,Standard_ND24s,Standard_DC2s,Standard_DC4s,Standard_HB120-16rs_v3,Standard_HB120-32rs_v3,Standard_HB120-64rs_v3,Standard_HB120-96rs_v3,Standard_HB120rs_v3,Standard_NV4as_v4,Standard_NV8as_v4,Standard_NV16as_v4,Standard_NV32as_v4,Standard_NC6s_v3,Standard_NC12s_v3,Standard_NC24rs_v3,Standard_NC24s_v3,Standard_PB6s,Standard_HB60rs,Standard_ND96asr_v4,Standard_ND40s_v3. Find out more on the valid VM sizes in each region at https://aka.ms/azure-regions.
Target: vmSize
yetunde@Azure:~$ az vm resize --resource-group ytarg --name webserver --size Standard_DS1_v2
{
  "additionalCapabilities": null,
  "applicationProfile": null,
  "availabilitySet": null,
  "billingProfile": null,
  "capacityReservation": null,
  "diagnosticsProfile": null,
  "evictionPolicy": null,
  "extendedLocation": null,
  "extensionsTimeBudget": null,
  "hardwareProfile": {
    "vmSize": "Standard_DS1_v2",
    "vmSizeProperties": null
  },
  "host": null,
  "hostGroup": null,
  "id": "/subscriptions/ebd0efd8-e011-4639-8831-641041145f77/resourceGroups/ytarg/providers/Microsoft.Compute/virtualMachines/webserver",
  "identity": null,
  "instanceView": null,
  "licenseType": null,
  "location": "eastus",
  "name": "webserver",
  "networkProfile": {
    "networkApiVersion": null,
    "networkInterfaceConfigurations": null,
    "networkInterfaces": [
      {
        "deleteOption": null,
        "id": "/subscriptions/ebd0efd8-e011-4639-8831-641041145f77/resourceGroups/ytarg/providers/Microsoft.Network/networkInterfaces/webserver400",
        "primary": null,
        "resourceGroup": "ytarg"
      }
    ]
  },
  "osProfile": {
    "adminPassword": null,
    "adminUsername": "akinboyt",
    "allowExtensionOperations": true,
    "computerName": "webserver",
    "customData": null,
    "linuxConfiguration": {
      "disablePasswordAuthentication": true,
      "patchSettings": {
        "assessmentMode": "ImageDefault",
        "patchMode": "ImageDefault"
      },
      "provisionVmAgent": true,
      "ssh": {
        "publicKeys": [
          {
            "keyData": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQCyCYvYPC0woksQn8suZw6VTpZe\r\nzqRumCRplxgDpMaQoXES4+w8UyWn2HTaZ+qcYiINw0pEouGpsahpLuCesHVb9Ug2\r\nK7lpRBPRmV7RXrYHJdR3ekpM9M1SKhvBszixL+rMKCg7l0h+v2LtjKZwmrhKOu9P\r\nFmIiTKVOMM5iFAZ/2C4W477k7zRjaiPAgVzsAqw8VYsR6IbslTcwr0kgDUYfV4ij\r\nsssN4mg5Ih7XqjQFaie0JM6NuoXNshA3Q63qlJEhXn2dm2auqSt13zhinKIasUO6\r\ncNhHBJDAbWKYltaEP5j6ZdLO6MbpvAp6eahCYyGsLKgFYcMkOzh1hy2Mg6uVnqF/\r\n3QFG+3CwHjHgtIc8RKji5oUz68SUfzOjM8kZYUw8wkHcyZRbR4+gr8TB1A2l1Ckb\r\nhtCaB/fzforyf9Z8XhA4Pmy9lrIVJ2OzVBjAQgF5xXrfSukzNFxNCeuZwIZ5LvO5\r\n4tzrfVCZBu5yX3McnJap17UflbsDFXhU4C9SRIU=generated-by-azure\r\n",
            "path": "/home/akinboyt/.ssh/authorized_keys"
          }
        ]
      }
    },
    "requireGuestProvisionSignal": true,
    "secrets": [],
    "windowsConfiguration": null
  },
  "plan": null,
  "platformFaultDomain": null,
  "priority": null,
  "provisioningState": "Succeeded",
  "proximityPlacementGroup": null,
  "resourceGroup": "ytarg",
  "resources": null,
  "scheduledEventsProfile": null,
  "securityProfile": null,
  "storageProfile": {
    "dataDisks": [
      {
        "caching": "None",
        "createOption": "Attach",
        "deleteOption": "Detach",
        "detachOption": null,
        "diskIopsReadWrite": null,
        "diskMBpsReadWrite": null,
        "diskSizeGb": null,
        "image": null,
        "lun": 0,
        "managedDisk": {
          "diskEncryptionSet": null,
          "id": "/subscriptions/ebd0efd8-e011-4639-8831-641041145f77/resourceGroups/ytarg/providers/Microsoft.Compute/disks/webserver_DataDisk_0",
          "resourceGroup": "ytarg",
          "storageAccountType": null
        },
        "name": "webserver_DataDisk_0",
        "toBeDetached": false,
        "vhd": null,
        "writeAcceleratorEnabled": false
      }
    ],
    "imageReference": {
      "exactVersion": "20.04.202111080",
      "id": null,
      "offer": "0001-com-ubuntu-server-focal",
      "publisher": "canonical",
      "sharedGalleryImageId": null,
      "sku": "20_04-lts",
      "version": "latest"
    },
    "osDisk": {
      "caching": "ReadWrite",
      "createOption": "FromImage",
      "deleteOption": "Detach",
      "diffDiskSettings": null,
      "diskSizeGb": null,
      "encryptionSettings": null,
      "image": null,
      "managedDisk": {
        "diskEncryptionSet": null,
        "id": "/subscriptions/ebd0efd8-e011-4639-8831-641041145f77/resourceGroups/ytarg/providers/Microsoft.Compute/disks/webserver_OsDisk_1_f0b9097a5cfe4011a0718ca583f32fe8",
        "resourceGroup": "ytarg",
        "storageAccountType": null
      },
      "name": "webserver_OsDisk_1_f0b9097a5cfe4011a0718ca583f32fe8",
      "osType": "Linux",
      "vhd": null,
      "writeAcceleratorEnabled": null
    }
  },
  "tags": null,
  "type": "Microsoft.Compute/virtualMachines",
  "userData": null,
  "virtualMachineScaleSet": null,
  "vmId": "c664c37a-f71c-447f-afc0-57fc92ca90a9",
  "zones": null
}
yetunde@Azure:~$ az vm start --resource-group ytarg --name webserver
yetunde@Azure:~$ az vm get-instance-view \
>     --name myVM \
>     --resource-group myResourceGroupVM \
>
{
  "additionalCapabilities": null,
  "applicationProfile": null,
  "availabilitySet": null,
  "billingProfile": null,
  "capacityReservation": null,
  "diagnosticsProfile": null,
  "evictionPolicy": null,
  "extendedLocation": null,
  "extensionsTimeBudget": null,
  "hardwareProfile": {
    "vmSize": "Standard_DS1_v2",
    "vmSizeProperties": null
  },
  "host": null,
  "hostGroup": null,
  "id": "/subscriptions/ebd0efd8-e011-4639-8831-641041145f77/resourceGroups/myResourceGroupVM/providers/Microsoft.Compute/virtualMachines/myVM",
  "identity": null,
  "instanceView": {
    "assignedHost": null,
    "bootDiagnostics": null,
    "computerName": "myVM",
    "disks": [
      {
        "encryptionSettings": null,
        "name": "myVM_disk1_bd1e46ab4eae44bcbb59cfb185b7de57",
        "statuses": [
          {
            "code": "ProvisioningState/succeeded",
            "displayStatus": "Provisioning succeeded",
            "level": "Info",
            "message": null,
            "time": "2021-11-19T13:20:48.973812+00:00"
          }
        ]
      }
    ],
    "extensions": null,
    "hyperVGeneration": "V1",
    "maintenanceRedeployStatus": null,
    "osName": "ubuntu",
    "osVersion": "18.04",
    "patchStatus": null,
    "platformFaultDomain": null,
    "platformUpdateDomain": null,
    "rdpThumbPrint": null,
    "statuses": [
      {
        "code": "ProvisioningState/succeeded",
        "displayStatus": "Provisioning succeeded",
        "level": "Info",
        "message": null,
        "time": "2021-11-19T13:21:02.161314+00:00"
      },
      {
        "code": "PowerState/running",
        "displayStatus": "VM running",
        "level": "Info",
        "message": null,
        "time": null
      }
    ],
    "vmAgent": {
      "extensionHandlers": [],
      "statuses": [
        {
          "code": "ProvisioningState/succeeded",
          "displayStatus": "Ready",
          "level": "Info",
          "message": "Guest Agent is running",
          "time": "2021-11-19T14:29:21+00:00"
        }
      ],
      "vmAgentVersion": "2.5.0.2"
    },
    "vmHealth": null
  },
  "licenseType": null,
  "location": "eastus",
  "name": "myVM",
  "networkProfile": {
    "networkApiVersion": null,
    "networkInterfaceConfigurations": null,
    "networkInterfaces": [
      {
        "deleteOption": null,
        "id": "/subscriptions/ebd0efd8-e011-4639-8831-641041145f77/resourceGroups/myResourceGroupVM/providers/Microsoft.Network/networkInterfaces/myVMVMNic",
        "primary": null,
        "resourceGroup": "myResourceGroupVM"
      }
    ]
  },
  "osProfile": {
    "adminPassword": null,
    "adminUsername": "azureuser",
    "allowExtensionOperations": true,
    "computerName": "myVM",
    "customData": null,
    "linuxConfiguration": {
      "disablePasswordAuthentication": true,
      "patchSettings": {
        "assessmentMode": "ImageDefault",
        "patchMode": "ImageDefault"
      },
      "provisionVmAgent": true,
      "ssh": {
        "publicKeys": [
          {
            "keyData": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDVl7syZc86aaq7CZjutR38SvGAdV/syT/tB9sJQFqes4nGzG6T3Ky9+iqo58f5Xq0AqyZJKrVX0f4VbGw+3hZOkFx6amTV4ZIOvk2heQIBO2lqc/gUmkB0uQ4PQC6E4LnCQLt7iyloeVgHFMSFYq862tIEV0qQZLoHfout4CH4U5VjJef/+I1c6V/iMiJ0wPNIgsQaIAZ2dHGzUEwbJ7ANbTF7EWPPPUfGCDBKGurlpKm5N+XnflXPrjtyIWHlvPu+7i3/bWvdt9iOpvgPz9i2PU70rRGOp49u83GDfDWlUqqLGWoTJ09SrIJk+OBQcwPuy9xmX/shS2xjPHHx1oHP",
            "path": "/home/azureuser/.ssh/authorized_keys"
          }
        ]
      }
    },
    "requireGuestProvisionSignal": true,
    "secrets": [],
    "windowsConfiguration": null
  },
  "plan": null,
  "platformFaultDomain": null,
  "priority": null,
  "provisioningState": "Succeeded",
  "proximityPlacementGroup": null,
  "resourceGroup": "myResourceGroupVM",
  "resources": null,
  "scheduledEventsProfile": null,
  "securityProfile": null,
  "storageProfile": {
    "dataDisks": [],
    "imageReference": {
      "exactVersion": "18.04.202111080",
      "id": null,
      "offer": "UbuntuServer",
      "publisher": "Canonical",
      "sharedGalleryImageId": null,
      "sku": "18.04-LTS",
      "version": "latest"
    },
    "osDisk": {
      "caching": "ReadWrite",
      "createOption": "FromImage",
      "deleteOption": "Detach",
      "diffDiskSettings": null,
      "diskSizeGb": 30,
      "encryptionSettings": null,
      "image": null,
      "managedDisk": {
        "diskEncryptionSet": null,
        "id": "/subscriptions/ebd0efd8-e011-4639-8831-641041145f77/resourceGroups/myResourceGroupVM/providers/Microsoft.Compute/disks/myVM_disk1_bd1e46ab4eae44bcbb59cfb185b7de57",
        "resourceGroup": "myResourceGroupVM",
        "storageAccountType": "Premium_LRS"
      },
      "name": "myVM_disk1_bd1e46ab4eae44bcbb59cfb185b7de57",
      "osType": "Linux",
      "vhd": null,
      "writeAcceleratorEnabled": null
    }
  },
  "tags": {},
  "type": "Microsoft.Compute/virtualMachines",
  "userData": null,
  "virtualMachineScaleSet": null,
  "vmId": "f65ad66d-6a56-4e4b-a2f5-42d502f14bc2",
  "zones": null
}
yetunde@Azure:~$ az vm get-instance-view \
>     --name webserver \
>     --resource-group ytarg \
>     --query instanceView.statuses[1] --output table
Code                Level    DisplayStatus
------------------  -------  ---------------
PowerState/running  Info     VM running
yetunde@Azure:~$ az vm list-ip-addresses --resource-group ytarg --name webserver --output table
VirtualMachine    PublicIPAddresses    PrivateIPAddresses
----------------  -------------------  --------------------
webserver         20.120.80.158        10.0.0.4
yetunde@Azure:~$ az vm stop --resource-group ytarg --name webserver
About to power off the specified VM...
It will continue to be billed. To deallocate a VM, run: az vm deallocate.
yetunde@Azure:~$ az vm start --resource-group ytarg --name webserver
yetunde@Azure:~$ az group delete --name ytarglab2 --no-wait --yes
yetunde@Azure:~$ az group delete --name ytarglab2 --no-wait --yes
(ResourceGroupNotFound) Resource group 'ytarglab2' could not be found.
Code: ResourceGroupNotFound
Message: Resource group 'ytarglab2' could not be found.
yetunde@Azure:~$ ls
clouddrive
yetunde@Azure:~$