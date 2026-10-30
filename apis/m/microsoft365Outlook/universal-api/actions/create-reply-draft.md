# Microsoft 365 Outlook: Create Reply Draft

Creates a draft reply to a message in Microsoft 365 Outlook, without sending it. The draft is pre-addressed to the original sender. Use Update Draft Message to change recipients, CC, subject, or body, then Send Draft Message to send it.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/create-reply-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/create-reply-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "AAMkAG..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/create-reply-draft', {
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
| `messageId` | string | yes | The ID of the Outlook message to create a reply draft for. Example: `AAMkAG...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bodyPreview": "string",
      "id": "string",
      "subject": "string",
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bodyPreview` | string | A text preview of the draft body. |
| `id` | string | The created reply draft message ID. |
| `subject` | string | The draft subject line. |
| `webLink` | string | A link to open the draft in Outlook on the web. |

## Native endpoint

Through the native Microsoft 365 Outlook API, this operation is `POST /v1.0/me/messages/{{messageId}}/createReply` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reply-draft.md) for the provider-specific parameters and requirements.

