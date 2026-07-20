# Datalyse: Edit Email Template

Updates an existing email template in Datalyse.

```
PUT https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/edit-email-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datalyse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/edit-email-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/edit-email-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | no | Template HTML content (optional) |
| `name` | string | no | Template name (optional) |
| `subject` | string | no | Default email subject (optional) |
| `templateId` | string | yes | ID of the template to edit |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | API response status |

## Native endpoint

Through the native Datalyse API, this operation is `POST /api/1.0/emails/templates/edit.json` (base URL `https://api.datalyse.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-email-template.md) for the provider-specific parameters and requirements.

