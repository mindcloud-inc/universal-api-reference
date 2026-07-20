# Zoom Team Chat: Mark Message Read Or Unread



```
PUT https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/mark-message-read-or-unread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/mark-message-read-or-unread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "me",
  "messageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/mark-message-read-or-unread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "me",
    "messageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The unique identifier of the user. Default: `me`. |
| `messageId` | string | yes | The unique identifier of the message. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoom Team Chat API returns.

## Native endpoint

Through the native Zoom Team Chat API, this operation is `PATCH /chat/users/:userId/messages/:messageId/status` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-message-read-or-unread.md) for the provider-specific parameters and requirements.

