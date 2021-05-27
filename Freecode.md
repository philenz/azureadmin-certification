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

### 1:41:56 [Azure Resource Manager](./freecode/AzureResourceManager.md)

### 2:08:58 [ARM Templates](./freecode/ARMTemplates.md)

### 2:32:16 [Storage Accounts](./freecode/StorageAccounts.md)

### 4:02:33 [Virtual Machines](./freecode/VirtualMachines.md)

### 5:31:35 [Disks](./freecode/Disks.md)

### 6:06:20 [Application Gateway](./freecode/ApplicationGateway.md)

### 6:13:20 [Scale Sets](./freecode/ScaleSets.md)

### 6:23:16 [Azure App Service](./freecode/AppService.md)

### 7:37:33 [Azure Monitor](./freecode/AzureMonitor.md)

### 8:15:39 [Backup Service](./freecode/BackupService.md)

### 8:31:18 [Azure Container Instances](./freecode/AzureContainerInstances.
md)

### 9:13:32 [Azure DNS](./freecode/AzureDNS.md)

### 9:30:05 [VNet](./freecode/VNet.md)
