# Zoho ZeptoMail: Add Template

Creates a new email template in Zoho ZeptoMail.

```
POST https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/add-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/add-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateName": "Ava Chen",
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/add-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateName": "Ava Chen",
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateName` | string | yes | Name of the template. |
| `templateAlias` | string | no | Optional alias for the template. |
| `subject` | string | yes | Template subject. |
| `htmlBody` | string | no | HTML template body. |
| `textBody` | string | no | Plain text template body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "description": "string",
        "modified_time": "2026-05-07T12:00:00.000Z",
        "subject": "string",
        "template_alias": "string",
        "template_key": "string",
        "template_name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.description` | string |  |
| `data.modified_time` | date |  |
| `data.subject` | string |  |
| `data.template_alias` | string |  |
| `data.template_key` | string |  |
| `data.template_name` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `POST agents/:agentAlias/templates` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-template.md) for the provider-specific parameters and requirements.

