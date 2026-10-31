# Bridgit Bench: Send Account Invitation



```
POST https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/send-account-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/send-account-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "groupingPermissions[].id": 1,
  "groupingPermissions[].groupId": 1,
  "email": "ava@example.com",
  "group": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/send-account-invitation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "groupingPermissions[].id": 1,
    "groupingPermissions[].groupId": 1,
    "email": "ava@example.com",
    "group": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The ID of the account |
| `groupingPermissions[]` | array<object> | no |  |
| `groupingPermissions[].id` | number | yes |  |
| `groupingPermissions[].groupId` | number | yes |  |
| `email` | string | yes |  |
| `group` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/invitations` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-account-invitation.md) for the provider-specific parameters and requirements.

