# Cloud 66: Create Database User

Creates a database user in your Cloud 66 account.

```
POST https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/create-database-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud 66 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/create-database-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stackId": "string",
  "serverGroupId": "string",
  "username": "Ava Chen",
  "userType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/create-database-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stackId": "string",
    "serverGroupId": "string",
    "username": "Ava Chen",
    "userType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stackId` | string | yes | Stack ID |
| `serverGroupId` | string | yes | Server group ID |
| `username` | string | yes | Database username to create |
| `databaseIds[]` | array<string> | no | Database UIDs to grant access to |
| `userType` | string | yes | Supported database user type |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloud 66 API returns.

## Native endpoint

Through the native Cloud 66 API, this operation is `POST /stacks/:stack_id/server_groups/:server_group_id/database_users` (base URL `https://app.cloud66.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-database-user.md) for the provider-specific parameters and requirements.

