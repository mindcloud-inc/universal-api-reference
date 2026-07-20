# Recombee: Set User Values

Updates values for a user in Recombee.

```
PUT https://connect.mindcloud.co/v1/universal/recombee/latest/actions/set-user-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recombee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recombee/latest/actions/set-user-values" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "user-123",
  "values": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recombee/latest/actions/set-user-values', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "user-123",
    "values": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cascadeCreate` | string | no |  |
| `userId` | string | yes | Example: `user-123`. |
| `values` | object | yes | Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Recombee API returns.

## Native endpoint

Through the native Recombee API, this operation is `POST /users/:userId` (base URL `https://rapi.recombee.com/{{credentials.databaseId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-user-values.md) for the provider-specific parameters and requirements.

