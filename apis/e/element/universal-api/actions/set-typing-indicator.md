# Element: Set Typing Indicator

Updates a room's typing indicator in Element.

```
PUT https://connect.mindcloud.co/v1/universal/element/latest/actions/set-typing-indicator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Element `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/element/latest/actions/set-typing-indicator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "string",
  "userId": "string",
  "typing": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/element/latest/actions/set-typing-indicator', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "string",
    "userId": "string",
    "typing": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | string | yes | Room ID to update. |
| `userId` | string | yes | Matrix user ID whose typing state should be updated. |
| `typing` | boolean | yes | Whether the user is currently typing. |
| `timeout` | number | no | Optional timeout in milliseconds for the typing notice. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Element API returns.

## Native endpoint

Through the native Element API, this operation is `PUT /_matrix/client/v3/rooms/:roomId/typing/:userId` (base URL `{{credentials.homeserverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-typing-indicator.md) for the provider-specific parameters and requirements.

