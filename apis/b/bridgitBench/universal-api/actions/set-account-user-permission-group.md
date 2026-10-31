# Bridgit Bench: Set Account User Permission Group



```
PUT https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/set-account-user-permission-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/set-account-user-permission-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "id": 1,
  "groupingPermissions[]": [
    {}
  ],
  "groupingPermissions[].id": 1,
  "groupingPermissions[].groupId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/set-account-user-permission-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "id": 1,
    "groupingPermissions[]": [{}],
    "groupingPermissions[].id": 1,
    "groupingPermissions[].groupId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `id` | number | yes | ID of the user to modify |
| `groupingPermissions[]` | array<object> | yes |  |
| `groupingPermissions[].id` | number | yes |  |
| `groupingPermissions[].groupId` | number | yes |  |
| `group` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `PUT /rp/api/v1/accounts/:accountId/users/:id/membership` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-account-user-permission-group.md) for the provider-specific parameters and requirements.

