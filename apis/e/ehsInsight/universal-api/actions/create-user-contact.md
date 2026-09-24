# EHS Insight: Create User Contact



```
POST https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/create-user-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EHS Insight `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/create-user-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ehsInsight/latest/actions/create-user-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userContactType` | list | no |  |
| `fullName` | string | no |  |
| `isEnabled` | number | no |  |
| `authProvider` | string | no |  |
| `username` | string | no |  |
| `emailAddress` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `businessEntity` | string | no |  |
| `employer` | string | no |  |
| `position` | string | no |  |
| `employeeId` | string | no |  |
| `roleAssignmentType` | string | no |  |
| `userRoles[]` | array<object> | no |  |
| `userRoles[].roleUid` | string | no |  |
| `userRoles[].businessEntity` | string | no |  |
| `securityGroups[]` | array<object> | no |  |
| `securityGroups[].securityGroup` | string | no |  |
| `securityGroups[].parameters[]` | array<object> | no |  |
| `securityGroups[].parameters[].templateParameter` | string | no |  |
| `securityGroups[].parameters[].businessEntities[]` | array<object> | no |  |
| `securityGroups[].parameters[].businessEntities[].item` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EHS Insight API returns.

## Native endpoint

Through the native EHS Insight API, this operation is `POST /v6/entity/UserContact/add` (base URL `https://{{credentials.companyName}}.ehsinsight.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user-contact.md) for the provider-specific parameters and requirements.

