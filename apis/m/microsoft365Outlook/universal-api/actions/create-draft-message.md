# Microsoft 365 Outlook: Create Draft Message

Creates a draft message in Microsoft 365 Outlook.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/create-draft-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/create-draft-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/create-draft-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `toRecipients[].emailAddress.address` | string | no | The email address to add as the draft recipient. Example: `jamie@mindcloud.co`. |
| `subject` | string | no | The draft email subject line. Example: `MindCloud Microsoft 365 draft test`. |
| `body.content` | string | no | The draft email body content. Example: `This is a draft email created by the MindCloud Microsoft 365 Outlook app.`. |

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
| `id` | string | The created draft message ID. |
| `subject` | string | The draft subject line. |
| `webLink` | string | A link to open the draft in Outlook on the web. |

## Native endpoint

Through the native Microsoft 365 Outlook API, this operation is `POST /v1.0/me/messages` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-message.md) for the provider-specific parameters and requirements.

