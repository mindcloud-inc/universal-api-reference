# Microsoft 365 Outlook: Reply to Message

Replies to a message in Microsoft 365 Outlook.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/reply-to-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/reply-to-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "AAMkAG..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/reply-to-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "AAMkAG..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | The ID of the Outlook message to reply to. Example: `AAMkAG...`. |
| `comment` | string | no | Optional text to include in the reply. Example: `Thanks - this is a reply test from the MindCloud Microsoft 365 Outlook app.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft 365 Outlook API returns.

## Native endpoint

Through the native Microsoft 365 Outlook API, this operation is `POST /v1.0/me/messages/{{messageId}}/reply` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reply-to-message.md) for the provider-specific parameters and requirements.

