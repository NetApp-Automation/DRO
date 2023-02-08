# NetApp Disaster Recovery Orchestrator (DRO)

NetApp’s DRO provides an ideal solution for customers who need a flexible solution for easy disaster recovery including a zero-compute footprint approach; it offers the benefits of a proven and trusted DR platform with the scale and flexibility of the public cloud. 

DRO leverages NetApp's SnapMirror replication-based approach for a powerful and economical solution for protecting data and applications running on VMware environments both on-premises and VMware Cloud on AWS integration with Amazon FSx for NetApp ONTAP.

## Documentation

Please refer to https://docs.netapp.com/us-en/netapp-solutions/ehc/dro/dro-overview.html for the official documentation.

# DRO Installation Steps

## Pre-requisites

- Following packages must be installed on the host machine (The script will install it if not already installed):
  - docker
  - docker-compose
  - jq
-	Connectivity to SRC and DST site vCenter and Storage systems
-	DNS resolution in place if using DNS names in place of IPs for vCenter/Storage systems
-	User with root permissions

**Note:** Recommended host OS: Ubuntu 20.04

## Installation Steps

1. Download the installation package on the designated virtual machine:

``` git clone https://github.com/NetApp-Automation/DRO.git ```

2. Unzip the package and navigate into the unziped folder:

``` tar -xf DRO-prereq.tar ```
``` cd dro_package ```

1. Run the deployment script and enter your host IP (for example: 10.10.10.10):

``` sudo sh deploy.sh ```

3. Once the script runs successfully, access the UI using below credentials:

**Username:** admin
**Password:** admin

## Troubleshooting Steps

1. If you encounter an error during initial installation, run the uninstallation script before retrying the installation again to cleanup any residual data. 
    
    ``` sudo sh uninstall.sh ```
  
2. If you encounter any issue post installation, please run the troubleshoot script and reach out to support from the UI.

    ``` sudo sh troubleshoot.sh ```
