# Microsoft 365: Forward Message

Forwards a message from Microsoft 365.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/forward-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/forward-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "AAMkAG..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/forward-message', {
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
| `messageId` | string | yes | The ID of the Outlook message to forward. Example: `AAMkAG...`. |
| `toRecipients[].emailAddress.address` | string | no | The email address to forward the message to. Example: `jamie@mindcloud.co`. |
| `comment` | string | no | Optional text to include above the forwarded message. Example: `Forwarding this message from the MindCloud Microsoft 365 app.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft 365 API returns.

## Native endpoint

Through the native Microsoft 365 API, this operation is `POST /v1.0/me/messages/{{messageId}}/forward` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/forward-message.md) for the provider-specific parameters and requirements.

