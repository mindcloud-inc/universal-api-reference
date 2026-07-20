# Mailtrap: Update Email Template

Updates an existing email template in Mailtrap.

```
PUT https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/update-email-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailtrap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/update-email-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/update-email-template', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "bodyHtml": "string",
      "bodyText": "string",
      "category": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "subject": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bodyHtml` | string |  |
| `bodyText` | string |  |
| `category` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `name` | string |  |
| `subject` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mailtrap API, this operation is `PATCH /email_templates/{email_template_id}` (base URL `https://mailtrap.io/api/accounts/:account_id`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-email-template.md) for the provider-specific parameters and requirements.

