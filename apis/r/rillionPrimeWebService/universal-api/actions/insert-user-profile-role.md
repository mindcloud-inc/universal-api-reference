# Rillion Prime Web Service: Insert User Profile Role

Insert a user profile role assignment into the Prime register queue. Administrative operation.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-user-profile-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-user-profile-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userProfileRole": {},
  "userProfileRole.loginName": "Ava Chen",
  "userProfileRole.userName": "Ava Chen",
  "userProfileRole.languageID": "string",
  "userProfileRole.email": "ava@example.com",
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-user-profile-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userProfileRole": {},
    "userProfileRole.loginName": "Ava Chen",
    "userProfileRole.userName": "Ava Chen",
    "userProfileRole.languageID": "string",
    "userProfileRole.email": "ava@example.com",
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userProfileRole` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, UserProfileRole section. |
| `userProfileRole.loginName` | string | yes | Loginname for SQL Server (Must be the same in the database) |
| `userProfileRole.userName` | string | yes | Username |
| `userProfileRole.languageID` | string | yes | Language setting. Case Sensitive, corresponding value in Language table and LanguageId column. |
| `userProfileRole.email` | string | yes | Email |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userProfileRole.userGroup` | string | no | Usergroup |
| `userProfileRole.validTo` | date | no | A valid to date for user access. |
| `userProfileRole.sID` | string | no | Foreign reference to user identity |
| `userProfileRole.role` | string | no | Role |
| `userProfileRole.roleName` | string | no | Rolename |
| `userProfileRole.roleUserGroup` | string | no | Rolegroup |
| `userProfileRole.active` | boolean | no | Active: 0=No, 1=Yes |
| `userProfileRole.includableInFlow` | boolean | no | Can role be inserted in a flow: 0=No; 1=Yes |
| `userProfileRole.roleSupervisor` | string | no | Role which is rolesupervisor. If this role is missing, the post will be created without this value. |
| `userProfileRole.powerRole` | string | no | The Rolemanager. If this role is missing, the post will be created without this value. |
| `userProfileRole.reminderArrival` | string | no | Send reminder x days after arrival. |
| `userProfileRole.reminderImmidiateBitCode` | number | no |  |
| `userProfileRole.reminderDueDate` | string | no | Send reminder X days before due date, 0 = inactive. |
| `userProfileRole.reminderSupervisor` | string | no | Send reminder to role supervisor after X days, 0 = inactive. |
| `userProfileRole.forwardSupervisor` | string | no | Transfer invoice to role supervisor after X days , 0 = Inactive. |
| `userProfileRole.authorizationAmount` | number | no | Authorization amount, invoice amount (TAX not included) |
| `userProfileRole.permissionGroupBitCode` | number | no | Permissiongroup |
| `userProfileRole.selectCompany` | string | no | Selection criteria for company permissions |
| `userProfileRole.selectAccount` | string | no | Selection criteria for account permissions |
| `userProfileRole.selectObject1` | string | no | Selection criteria for objecttype1 permissions |
| `userProfileRole.selectObject2` | string | no | Selection criteria for objecttype2 permissions |
| `userProfileRole.selectObject3` | string | no | Selection criteria for objecttype3 permissions |
| `userProfileRole.selectObject4` | string | no | Selection criteria for objecttype4 permissions |
| `userProfileRole.selectObject5` | string | no | Selection criteria for objecttype5 permissions |
| `userProfileRole.selectObject6` | string | no | Selection criteria for objecttype6 permissions |
| `userProfileRole.selectObject7` | string | no | Selection criteria for objecttype7 permissions |
| `userProfileRole.selectObject8` | string | no | Selection criteria for objecttype8 permissions |
| `userProfileRole.selectCommodity` | string | no | Selection criteria for commodity permissions |
| `userProfileRole.selectExpenseType` | string | no | Selection criteria for expense type permissions |
| `userProfileRole.removePermissions` | boolean | no | Shall role permissions be removed if role is set as inactive: 0=No, 1=Yes |
| `userProfileRole.group1` | string | no | Optional groupfield 1 |
| `userProfileRole.group2` | string | no | Optional groupfield 2 |
| `userProfileRole.group3` | string | no | Optional groupfield 3 |
| `userProfileRole.defaultCompany` | string | no | Default Company setting for Capex request, Requisition and Expense. |
| `userProfileRole.defaultObject1` | string | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRole.defaultObject2` | string | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRole.defaultObject3` | string | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRole.defaultObject4` | string | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRole.defaultObject5` | string | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRole.defaultObject6` | string | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRole.defaultObject7` | string | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRole.defaultObject8` | string | no | Default ObjectValue setting for Capex request, Requisition and Expense. |
| `userProfileRole.logInvoiceAccess` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-user-profile-role.md) for the provider-specific parameters and requirements.

