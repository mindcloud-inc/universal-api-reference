# Outlook: Send Draft Message

Sends an existing draft email from Outlook.

```
POST https://connect.mindcloud.co/v1/universal/outlook/latest/actions/send-draft-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outlook/latest/actions/send-draft-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outlook/latest/actions/send-draft-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | Microsoft Graph ID of the draft message to send. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Outlook API returns.

## Native endpoint

Through the native Outlook API, this operation is `POST /me/messages/:messageId/send` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-draft-message.md) for the provider-specific parameters and requirements.

