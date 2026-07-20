# Leantime: Update User



```
PUT https://connect.mindcloud.co/v1/universal/leantime/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1,
  "params.values.user": "string",
  "params.values.role": 1,
  "params.values.status": "a",
  "params.values.clientId": "0",
  "params.values.firstname": "Ava",
  "params.values.lastname": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leantime/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1,
    "params.values.user": "string",
    "params.values.role": 1,
    "params.values.status": "a",
    "params.values.clientId": "0",
    "params.values.firstname": "Ava",
    "params.values.lastname": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | The Leantime user id to update. |
| `params.values.user` | string | yes | Username or email for the user. |
| `params.values.role` | number | yes | Numeric role key for the user. |
| `params.values.status` | string | yes | User status code. Default: `a`. |
| `params.values.clientId` | number | yes | Client id assigned to the user. Default: `0`. |
| `params.values.firstname` | string | yes | User first name. |
| `params.values.lastname` | string | yes | User last name. |
| `params.values.phone` | string | no | User phone number. |
| `params.values.password` | string | no | Optional replacement password. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leantime API returns.

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

