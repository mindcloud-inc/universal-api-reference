# EHS Insight: Update User Contact



```
PUT https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/update-user-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EHS Insight `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/update-user-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rowUid": "string",
  "changeToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/update-user-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rowUid": "string",
    "changeToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rowUid` | string | yes | RowUID from Get User Contact. |
| `changeToken` | string | yes | Use the unchanged ChangeToken from the freshly fetched full record. |
| `fullName` | string | no |  |
| `isEnabled` | number | no | Preserve the fetched numeric value unless changing enabled status intentionally. |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `businessEntity` | string | no | RowUID of the business entity. |
| `employer` | string | no | RowUID from the Employer entity list. |
| `position` | string | no | RowUID from the Position entity list. |
| `employeeId` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userContactNumber` | string | no | Preserve the fetched value. |
| `userContactType` | string | no | Preserve the fetched value. Do not reset a user to Contact when an administrator has converted the record. |
| `gender` | string | no |  |
| `birthDate` | date | no | Example: `2026-01-15`. |
| `hireDate` | date | no | Example: `2026-01-15`. |
| `positionStartDate` | date | no | Example: `2026-01-15`. |
| `industryStartDate` | date | no | Example: `2026-01-15`. |
| `homeAddress` | string | no |  |
| `homeCity` | string | no |  |
| `homeState` | string | no |  |
| `homeZip` | string | no |  |
| `phoneNumber` | string | no |  |
| `authProvider` | string | no | Preserve the fetched authentication provider. API version 6 uses Password for password authentication. |
| `username` | string | no |  |
| `emailAddress` | string | no |  |
| `roleAssignmentType` | string | no | Preserve the fetched role assignment mode: DirectAssignment uses User Roles; SecurityGroups uses Security Groups. |
| `userRoles[]` | array<object> | no | Preserve the complete fetched direct-role assignments. |
| `userRoles[].roleUid` | string | no |  |
| `userRoles[].businessEntity` | string | no | Role-scoped Business Entity. Preserve null for roles that apply across all entities. |
| `securityGroups[]` | array<object> | no | Preserve the complete fetched group assignments and parameters. |
| `securityGroups[].securityGroup` | string | no |  |
| `securityGroups[].parameters[]` | array<object> | no |  |
| `securityGroups[].parameters[].templateParameter` | string | no |  |
| `securityGroups[].parameters[].businessEntities[]` | array<object> | no |  |
| `securityGroups[].parameters[].businessEntities[].item` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EHS Insight API returns.

## Native endpoint

Through the native EHS Insight API, this operation is `POST /v6/entity/UserContact/update` (base URL `https://{{credentials.companyName}}.ehsinsight.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-contact.md) for the provider-specific parameters and requirements.

