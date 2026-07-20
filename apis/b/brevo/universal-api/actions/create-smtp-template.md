# Brevo: Create SMTP Template



```
POST https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-smtp-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-smtp-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "htmlContent": "string",
  "replyTo": "string",
  "senderName": "Ava Chen",
  "subject": "string",
  "templateName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-smtp-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "htmlContent": "string",
    "replyTo": "string",
    "senderName": "Ava Chen",
    "subject": "string",
    "templateName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `htmlContent` | string | yes | HTML content for the template. |
| `replyTo` | string | yes | Reply-to email address. |
| `senderName` | string | yes | Display name of the template sender. |
| `subject` | string | yes | Default subject line for the template. |
| `templateName` | string | yes | Name of the SMTP template. |
| `toField` | string | no | Template to-field value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Brevo API, this operation is `POST /v3/smtp/templates` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-smtp-template.md) for the provider-specific parameters and requirements.

