# Introduction

Students will learn how to setup and configure a Virtual Network with Subnets in Azure. Students will also learn how to secure the Virtual Network with Firewall rules and route tables. Additionally, students will set up access to the Virtual Network with a "jump box" and a Site-to-Site VPN connection.
# Sign-up for Workshop Environment

To make it easier for you to work on the labs, you are provided with pre-provisioned Azure environment. You will receive sign-up link for the lab environment from your instructor. 

* Register for the lab environment by providing your information and clicking on **Submit** button.

* On the next page, click the **Launch Lab** button.
 
* Wait for the lab environment to be provisioned. Sometimes this can take upto **10 minutes**. Once environment provisioning is complete, you will receive details in email as well as in the browser.
 
 > Note: Lab environment is enabled only for specific duration or workshop end time - whichever is earlier. At the end of the allowed time, environment will be self-destructed. Also, for multi-day workshops, all virtual machines will be shutdown at 7 PM local time and start at 8AM local time.

# Verify the pre-provisioned Environment

* Users can use the **Azure Credentials** given to them to login to the Azure Portal
* Verify seven resource groups.
* Resource Group **ODL_ecn-29907-LabVMRG** will be already created in the users Azure Environment with the LABVM deployed in it.
* **LABVM** has been configured with the following:
  1. IE Enhanced Security has been disabled
  2. Support files are downloaded into the directory C:\ECN-Hackathon
  3. Azure PowerShell
* Users can select **LABVM** and click on **Connect** to download the RDP file
* Open the RDP file to connect to the LABVM. Provide the credentials you received to login to the VM
* Once you login to the LABVM, server manager will open. Select Local Server and verify that IE Enhanced Security Configuration has also been turned off
* Now, go to C:\ECN-Hackathon directory and verify the student files are there 

## Verify Azure Access

Open a browser instance in private or incognito mode and login to [Microsoft Azure Portal](https://portal.azure.com) using the credentials provided.

> Note: You might have an existing Azure Credential. For the pre-provisioned environment, new Microsoft Azure environment is provisioned and new AAD user is created for you. To prevent conflict with your existing accounts, it is advised to use In Private mode of IE / IE Edge or Incognito mode of Chrome browser.

## Verify Virtual Machine

You are provided a Visual Studio Community 2017 on Windows Server 2016 (x64)Microsoft with additional softwares configured. FQDN of the LABVM virtual machine and administrator credentials are provided in the lab details page. You can remote into the virtual machine using the provided credentials.

# Known Issues
### Connecting DSVM with RDP having issue addresses CredSSP

> **Possible Solutions**:

* With the release of the March 2018 Security bulletin, there was a fix that addressed a CredSSP, “Remote Code Execution” vulnerability (CVE-2018-0886) which could impact RDP connections. 
**Resolution**
Please follow the instruction under https://github.com/SpektraSystems/Microsoft-Cloud-Workshop/blob/master/RDP%20CredSSP/README.md

# Notes to Instructors / Proctors
* Resource Group **ODL-enc-29907-LabVMRG** having LABVM. User will not deply anything in this resource group. **29907** is unique for each user and will very for each user.
* As users doesn't have permissions to create new **resource group**. They should choose existing resource groups as all the resouce groups have already created.
* Each resource group have prefix **ODL_ecn-29907-**, 
* **Ex:** In Task 1 of Exercise 1, choose existing RG **ODL-enc-29907-WGVNetRG1** instead of creating new RG to deploy virtual network **WGVNet1**. Use similar for other RGs.
  - Make sure to deploy all Resources in RG location Ex: If resource group is in **West US** then deploy **virtual network in West US** only. 
* In Task 1 of Exercise 2, use existing RG **ODL-enc-29907-WGVNetRG2** instead of creating new RG to deploy virtual network **WGVNet2**.
  - Make sure to deploy all Resources in RG location Ex: If resource group is in **West US** then deploy **virtual network in West US** only. 
* In Task 1 of Exercise 4, use existing RG **ODL_ecn-29907-WGVMRGTMT** instead of creating new RG to deploy template **n-tier application**
  * Edit following template parameters values:    
  * existingVirtualNetworkName: **WGVNet2**    
  * existingVirtualNetworkResourceGroup: **ODL_ecn-29907-WGVNetRG2**, **29907** will very with each user.
* In Task 1 of Exercise 5, choose existing RG **ODL_ecn-29907-WGMGMTRG** instead of creating new RG to deploy management VM Windows Server 2016 Datacenter. Use **Standard F1S** size for virtual machine inthis step.
* In Task 1 of Exercise 7, choose existing RG **ODL_ecn-29907-baracudafw** instead of creating new RG to deploy cloudgen firewall for azure BYOL (VM)
* In Task 1 of Exercise 9, choose existing RG **ODL_ecn-29907-OnPremVNet** instead of creating new RG to deploy **on-prem virtual network**
  * Deploy On-prem Virtual Network in **different region** region istead of  using RG location.
* Users should **use** the **Azure Credentials** given to them to login to **Visual Studio**

# Help and Support

If you require any help during the workshop, please reach out to the instructor / proctors. Instructors / proctors might escalate the issue to remote support team, at that time, please pass on your **AAD User ID** (aad_user_xyz), so that it is easier to look up your environment.
