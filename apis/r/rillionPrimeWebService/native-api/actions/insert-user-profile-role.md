# Insert User Profile Role with Rillion Prime Web Service

Insert a user profile role assignment into the Prime register queue. Administrative operation.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userProfileRoleQueueDTO` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, UserProfileRole section. |
| `userProfileRoleQueueDTO.LoginName` | body | `string` | yes | Loginname for SQL Server (Must be the same in the database) |
| `userProfileRoleQueueDTO.UserName` | body | `string` | yes | Username |
| `userProfileRoleQueueDTO.UserGroup` | body | `string` | no | Usergroup |
| `userProfileRoleQueueDTO.LanguageID` | body | `string` | yes | Language setting. Case Sensitive, corresponding value in Language table and LanguageId column. |
| `userProfileRoleQueueDTO.ValidTo` | body | `date` | no | A valid to date for user access. |
| `userProfileRoleQueueDTO.Email` | body | `string` | yes | Email |
| `userProfileRoleQueueDTO.SID` | body | `string` | no | Foreign reference to user identity |
| `userProfileRoleQueueDTO.Role` | body | `string` | no | Role |
| `userProfileRoleQueueDTO.RoleName` | body | `string` | no | Rolename |
| `userProfileRoleQueueDTO.RoleUserGroup` | body | `string` | no | Rolegroup |
| `userProfileRoleQueueDTO.Active` | body | `boolean` | no | Active: 0=No, 1=Yes |
| `userProfileRoleQueueDTO.IncludableInFlow` | body | `boolean` | no | Can role be inserted in a flow: 0=No; 1=Yes |
| `userProfileRoleQueueDTO.RoleSupervisor` | body | `string` | no | Role which is rolesupervisor. If this role is missing, the post will be created without this value. |
| `userProfileRoleQueueDTO.PowerRole` | body | `string` | no | The Rolemanager. If this role is missing, the post will be created without this value. |
| `userProfileRoleQueueDTO.ReminderArrival` | body | `string` | no | Send reminder x days after arrival. |
| `userProfileRoleQueueDTO.ReminderImmidiateBitCode` | body | `number` | no | — |
| `userProfileRoleQueueDTO.ReminderDueDate` | body | `string` | no | Send reminder X days before due date, 0 = inactive. |
| `userProfileRoleQueueDTO.ReminderSupervisor` | body | `string` | no | Send reminder to role supervisor after X days, 0 = inactive. |
| `userProfileRoleQueueDTO.ForwardSupervisor` | body | `string` | no | Transfer invoice to role supervisor after X days , 0 = Inactive. |
| `userProfileRoleQueueDTO.AuthorizationAmount` | body | `number` | no | Authorization amount, invoice amount (TAX not included) |
| `userProfileRoleQueueDTO.PermissionGroupBitCode` | body | `number` | no | Permissiongroup |
| `userProfileRoleQueueDTO.SelectCompany` | body | `string` | no | Selection criteria for company permissions |
| `userProfileRoleQueueDTO.SelectAccount` | body | `string` | no | Selection criteria for account permissions |
| `userProfileRoleQueueDTO.SelectObject1` | body | `string` | no | Selection criteria for objecttype1 permissions |
| `userProfileRoleQueueDTO.SelectObject2` | body | `string` | no | Selection criteria for objecttype2 permissions |
| `userProfileRoleQueueDTO.SelectObject3` | body | `string` | no | Selection criteria for objecttype3 permissions |
| `userProfileRoleQueueDTO.SelectObject4` | body | `string` | no | Selection criteria for objecttype4 permissions |
| `userProfileRoleQueueDTO.SelectObject5` | body | `string` | no | Selection criteria for objecttype5 permissions |
| `userProfileRoleQueueDTO.SelectObject6` | body | `string` | no | Selection criteria for objecttype6 permissions |
| `userProfileRoleQueueDTO.SelectObject7` | body | `string` | no | Selection criteria for objecttype7 permissions |
| `userProfileRoleQueueDTO.SelectObject8` | body | `string` | no | Selection criteria for objecttype8 permissions |
| `userProfileRoleQueueDTO.SelectCommodity` | body | `string` | no | Selection criteria for commodity permissions |
| `userProfileRoleQueueDTO.SelectExpenseType` | body | `string` | no | Selection criteria for expense type permissions |
| `userProfileRoleQueueDTO.RemovePermissions` | body | `boolean` | no | Shall role permissions be removed if role is set as inactive: 0=No, 1=Yes |
| `userProfileRoleQueueDTO.Group1` | body | `string` | no | Optional groupfield 1 |
| `userProfileRoleQueueDTO.Group2` | body | `string` | no | Optional groupfield 2 |
| `userProfileRoleQueueDTO.Group3` | body | `string` | no | Optional groupfield 3 |
| `userProfileRoleQueueDTO.DefaultCompany` | body | `string` | no | Default Company setting for Capex request, Requisition and Expense. |
| `userProfileRoleQueueDTO.DefaultObject1` | body | `string` | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRoleQueueDTO.DefaultObject2` | body | `string` | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRoleQueueDTO.DefaultObject3` | body | `string` | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRoleQueueDTO.DefaultObject4` | body | `string` | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRoleQueueDTO.DefaultObject5` | body | `string` | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRoleQueueDTO.DefaultObject6` | body | `string` | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRoleQueueDTO.DefaultObject7` | body | `string` | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRoleQueueDTO.DefaultObject8` | body | `string` | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRoleQueueDTO.LogInvoiceAccess` | body | `boolean` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
