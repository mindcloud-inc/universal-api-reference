# Microsoft 365 Outlook: Create Forward Draft

Creates a draft forward of a message in Microsoft 365 Outlook, without sending it. Use Update Draft Message to change recipients, CC, subject, or body, then Send Draft Message to send it.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/create-forward-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/create-forward-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "AAMkAG...",
  "toRecipients": "jamie@mindcloud.co, other@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/create-forward-draft', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "AAMkAG...",
    "toRecipients": "jamie@mindcloud.co, other@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | The ID of the Outlook message to create a forward draft for. Example: `AAMkAG...`. |
| `toRecipients` | string | yes | Comma-separated email addresses to forward the draft to. Example: person@example.com, other@example.com Example: `jamie@mindcloud.co, other@mindcloud.co`. |
| `comment` | string | no | Optional text to include above the forwarded message. Example: `Forwarding this message from the MindCloud Microsoft 365 Outlook app.`. |

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
| `id` | string | The created forward draft message ID. |
| `subject` | string | The draft subject line. |
| `webLink` | string | A link to open the draft in Outlook on the web. |

## Native endpoint

Through the native Microsoft 365 Outlook API, this operation is `POST /v1.0/me/messages/{{messageId}}/createForward` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-forward-draft.md) for the provider-specific parameters and requirements.

