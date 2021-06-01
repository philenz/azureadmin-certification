## Test 4
* If an AAD global admin creates a directory, no other admins can add users as no role assigned.
* Azure SQL databases don't use Azure Backup
* Log analytics workspace does not need to be in the same region as the recovery services vault
* Once you add a `cloud endpoint` to a sync group you cant add any other shares as the cloud endpoint
* Can only have more than one `server endpoint` if namespaces are on the same volume
* Add phone numbers to AD users if need to enable MFA
* Convert guest users to regular users if need to enable MFA
* `kubenet` = default
* `azure container network interface` = every pod gets an ip from the subnet
* ```kusto
  search in (Event) "error"
  | take 10
  ```
* Can move resources across resource groups in different regions
* availability set max fault domains = __3__
* max machines can add at once = __20__
* policy assigned at subscription level overrides lower level (e.g.: resource group)
