# configure-and-manage-secrets
Configure and manage secrets in Azure Key Vault

---

# Introduction
Storing and handling secrets, encryption keys, and certificates directly is risky, and every usage introduces the possibility of unintentional data exposure. Azure Key Vault provides a secure storage area for managing all your app secrets so you can properly encrypt your data in transit or while it's being stored.

--- 

# Objectives
Implementing key vault helps is helpful in developing a security and compliance plan.   
This projects takes a look at:
- Explore proper usage of Azure Key Vault 
- Manage access to an Azure Key Vault
- Explore certificate management with Azure Key Vault
- Configure a Hardware Security Module Key-generation solution

--- 

# Services deployed
<!--- Microsoft Azure -->
<!-- Key Vaults --> 
![](Key-Vaults.png)

--- 

# Azure Key Vaults in summary
- What is Azure Key Vault?   
Azure Key Vault is a cloud service for securely storing and accessing secrets. It is a centralized cloud service for storing application secrets such as encryption keys, certificates, and server-side tokens. 

- What are secrets?   
A secret is anything that you want to tightly control access to, such as API keys, passwords, certificates (.PFX files), or cryptographic keys. 

- What is an HSM?   
HSM is one of several key management solutions in Azure.Azure Key Vault Managed HSM (Hardware Security Module) is a fully managed, highly available, single-tenant, standards-compliant cloud service that enables you to safeguard cryptographic keys for your cloud applications, using FIPS 140-2 Level 3 validated HSMs.   

- Below are some benefits of deploying/utilizing Azure Key Vaults   
⚡ Key Vault helps you control your applications' secrets by keeping them in a single central location and providing secure access, permissions control, and access logging.   
⚡ Helps securely store and tightly control access to tokens, passwords, certificates, API keys, and other secrets.   
⚡ Useful as a Key Management solution which allows for easy creation and control of encryption keys used to encrypt your data.   
⚡ Allows easy provision and management of public and private Transport Layer Security/Secure Sockets Layer (TLS/SSL) certificates for use with Azure and your internal connected resources.   
Other benefits include:   
⚡ Centralizing storage of application secrets in Azure Key Vault allows you to control their distribution.   
⚡ Access to a key vault requires proper authentication and authorization before a caller (user or application) can get access.   
⚡ Monitoring - You have control over your logs and you may secure them by restricting access and you may also delete logs that you no longer need.   
⚡ AKV simplifies administration of application secrets and also affords one the opportunity to secrets with other Azure services. 

---

# Steps 
Creating a vault in the Azure portal requires no initial configuration.   
Your signed-in user identity is automatically granted the full set of secret management permissions, and you can start adding secrets immediately.   
Once you have a vault, adding and managing secrets can be done from any Azure administrative interface, including the Azure portal, the Azure CLI, and Azure PowerShell.   

- Create a new Azure Key Vault   
![](kv1a.png)   

- Add a secret   
![](kv2.png)   

- Show the secret   
![](kv3.png)   

- Sample certificate   
![](kv6.png) 

# Other ways to consume the secret   
You can create and retrieve secrets from the Azure Key Vault as long as you're authenticated with Azure AD using the REST API, native SDKs, Azure CLI, or Azure PowerShell.   
For example, this can be done using Azure PowerShell:   
- "Get-AzKeyVault" which returns the following
![](kv4.png)   

- Get-AzKeyVaultSecret -VaultName 'VaultamortDiary' -Name 'HiddenLocation'
![](kv5.png)   

---

# Summary
- That sums up creating a Key Vault with an example of generating/importing a Key, secrete or certificate for safe keeping. 
- Other associated tasks: secrets can be further managed using the Azure Portal, Azure CLI and various programming languages to create Key Vaults, set, and retrieve secrets.

---

# References/Credits:
- https://learn.microsoft.com/en-us/azure/key-vault/general/basic-concepts
- https://learn.microsoft.com/en-us/training/modules/configure-and-manage-azure-key-vault/
