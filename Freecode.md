## [AZ-104: freeCodeCamp.org](https://www.youtube.com/watch?v=10PbGbTUSAg)

### 0:19:47 [Azure Active Directory](./freecode/AzureAD.md)
* 4 editions of AAD...
  1. Free
  1. 365
  1. Premium 1 _conditional access_,  _custom roles_
  1. Premium 2 _Intune_, _custom roles_
* `AD DS` provides managed domain services...
  - domain join
  - group policy
  - ldap
  - ntlm
* `AD Connect` connects on-prem AD to Azure, featuring...
  - password hash synchronization
  - pass-through authentication
  - federation integration
  - synchronization
  - health monitoring `Azure AD Connect Health`
* AD Assigning access rights...
  - direct
  - group
  - rule-based
  - external authority assignment
### 0:57:29 [Device Management](./freecode/DeviceManagement.md)
* Join devices to AAD in three ways...
  1. Azure AD registered: `personal`
  1. Azure AD joined: `organisation`
  1. Hybrid Azure AD joined: `organisation`
     - signed in with an AD DS account
* MDM / MAM are managed by `Microsoft Intune`
* Use `Windows Autopilot` to set up and preconfigure new devices

### 1:13:35 [Azure Roles](./freecode/AzureRoles.md)
* 3 types of roles...
  1. classic subscription administrator role
      1. account administrator
      1. service administrator
      1. co-administrator
  1. Azure roles = RBAC = built on top of ARM
      1. `BuiltInRole`
      1. `CustomRole`
  1. AAD roles = manage AAD resources
      1. `BuiltInRole`
          1. global administrator
          1. user administrator
          1. billing administrator
      1. `CustomRole`
* RBAC role assignment consists of 3 elements...
  1. security principal
      1. user
      1. group
      1. service principal
      1. managed identity
  1. role definition, 4 builtin...
      1. owner (all perms)
      1. contributor (no grant perms)
      1. reader
      1. user access administrator (only grant perms)
  1. scope
### 1:28:40 [Azure Policies](./freecode/AzurePolicies.md)
* Define using a Policy definition JSON file
* Assign to a user, resource group, or management group
* Policy initiative = group of policies
### 1:41:56 [Azure Resource Manager](./freecode/AzureResourceManager.md)
* Resource lock levels = `CanNotDelete` and `ReadOnly`
* Must register `Resource Providers` to use Azure resources
* `Azure Blueprints` = kind of an enterprise-level `ARM Templates`
  - Governed subscriptions
  - Improved tracking and auditing of deployments
  - Backed by Azure Cosmos DB, objects replicated to multiple regions
### 2:08:58 [ARM Templates](./freecode/ARMTemplates.md)
* Declarative
* Template functions
* User-defined functions
### 2:32:16 [Storage Accounts](./freecode/StorageAccounts.md)
* SMB 445
* Standard storage access tiers...
  1. __Cool__
  1. __Hot__ stored for >=30 days
  1. __Archive__ stored for >=180 days
* When moving from a cooler tier, cost is write operation to destination tier
* When moving from a hotter tier, cost is read operation from source tier
* Levels of redundancy [3 copies, synchronously updated]
  1. $ Primary region redundancy
      - LRS: 11 9s durability
      - ZRS: 12 9s
  1. $$ Secondary region redundancy (GRS, GZRS)
  1. $$$ Secondary region redundancy with read access
      - RA-GRS: 16 9s
      - RA-GZRS: 16 9s
* Blob types = 
  1. block
  1. append
  1. page
* Azure Files backup (shared snapshots)
  - readonly
  - up to 200 snapshots
  - retain for up to 10 years
  - stored in your file share... doh!
* ATP = advanced threat protection if something dodgy happening!
* Azure Files identity...
    1. Join storage to an `on-premise` AD domain service
    2. Join storage to a `Microsoft managed` AD domain service
    3. Mount using storage account name and key
* Shared Access Signatures
    1. account-level
    1. service-level
    1. user delegated (e.g.: storage account)
    1. ad-hoc any of the above plus uri parameters for start/end time, and permissions
* Import/Export use `WAImportExport`
    - import to blob or files
    - export from blob
### 4:02:33 [Virtual Machines](./freecode/VirtualMachines.md)
* ACU = Azure compute unit, Standard_A1 = 100
* Can use Azure Automations to patch (Update Management)
### 5:31:35 [Disks](./freecode/Disks.md)
* 3 9s availability
* 3x copies
* Encryption...
  1. SSE
  1. ADE (Azure Disk encryption) = encrpyt using BitLocker or DM-Crypt
* Disk Bursting allows boosting of disk iops performance for a period of time
  ### 6:06:20 [Application Gateway](./freecode/ApplicationGateway.md)
* private ip = internal lb
* frontend --> routing rules --> backend pools (or can set target type to a redirect)
* listener types...
  1. basic: forward all requests
  1. multi-site: forward based on host header and host name
### 6:13:20 [Scale Sets](./freecode/ScaleSets.md)
* Scale-In policy
  1. Default (delete vm with highest instance id)
  1. Newest VM
  1. Oldest VM
* 2 types of health monitoring...
  1. application health extension
  1. load balancer probe
### 6:23:16 [Azure App Service](./freecode/AppService.md)
* Elastic Beanstalk
* Can do containers, too
* And has idea of deployment slots
* ASE = fully isolated and dedicared version for high scale
* Can deploy from lots of sources including `Kudu`
* Can also run `WebJobs`
### 7:37:33 [Azure Monitor](./freecode/AzureMonitor.md)
* CloudWatch
* Azure Monitor Logs
* Azure Monitor Metrics
* Log Analytics lets you run KQL queries against Azure Monitor Logs
* Metrics Explorer
* Alerts
* Azure Dashboards
* Azure Workbooks are for data analysis
* Application Insights is an APM
### 8:15:39 [Backup Service](./freecode/BackupService.md)
* Azure Recovery Services (MARS) vault stores backups of vms and databases
* Stick a MARS agent on on-premise
### 8:31:18 [Azure Container Instances](./freecode/AzureContainerInstances.md)
* Multi-container groups only supported in linux
* Container restart policies... always, never, onfailure
* Can mount azure files
* `ACR Tasks` allows automation of OS and framework patching
### 9:13:32 [Azure DNS](./freecode/AzureDNS.md)
### 9:30:05 [VNet](./freecode/VNet.md)
* VPN Gateway topologies...
  1. `Site-to-Site`: when you connect azure to an on-premise data center
  1. `Multi-Site`: when you connect azure to multiple on-premice data centers
  1. `Point-to-Site`: connect azure to multiple individual computers
  1. `VNet-to-VNet`