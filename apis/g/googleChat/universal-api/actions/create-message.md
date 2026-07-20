# Google Chat: Create Message

Creates a message in a Google Chat space.

```
POST https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "space": "4Oe1TyAAAAE",
  "text": "Hello from MindCloud"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/create-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "space": "4Oe1TyAAAAE",
    "text": "Hello from MindCloud"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `space` | string | yes | Enter only the space ID from the List Spaces result. If the result shows spaces/4Oe1TyAAAAE, enter 4Oe1TyAAAAE here. Example: `4Oe1TyAAAAE`. |
| `threadKey` | string | no | Optional thread key for replies or new threads. Example: `incident-123`. |
| `requestId` | string | no | Optional idempotency key for this message request. Example: `mc-chat-001`. |
| `messageReplyOption` | string | no | Optional reply behavior for named spaces. |
| `messageId` | string | no | Optional custom message ID. Example: `client-message-001`. |
| `text` | string | yes | Plain-text message body to send to the selected Google Chat space. With user OAuth, messages are sent as the connected Google user. Example: `Hello from MindCloud`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Chat API returns.

## Native endpoint

Through the native Google Chat API, this operation is `POST /spaces/:space/messages` (base URL `https://chat.googleapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.

