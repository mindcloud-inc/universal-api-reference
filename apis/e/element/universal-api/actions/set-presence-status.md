# Element: Set Presence Status

Updates a user's presence status in Element.

```
PUT https://connect.mindcloud.co/v1/universal/element/latest/actions/set-presence-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Element `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/element/latest/actions/set-presence-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "presence": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/element/latest/actions/set-presence-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "presence": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | Matrix user ID to update. |
| `presence` | string | yes | Presence state to publish. |
| `statusMessage` | string | no | Optional status message to publish. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Element API returns.

## Native endpoint

Through the native Element API, this operation is `PUT /_matrix/client/v3/presence/:userId/status` (base URL `{{credentials.homeserverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-presence-status.md) for the provider-specific parameters and requirements.

