# Insighto.ai: Upsert Contact By Email Or Phone Number



```
POST https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/upsert-contact-by-email-or-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/upsert-contact-by-email-or-phone-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Taylor",
  "lastName": "Jones",
  "email": "taylor@example.com",
  "phoneNumber": "+15551234567"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/upsert-contact-by-email-or-phone-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Taylor",
    "lastName": "Jones",
    "email": "taylor@example.com",
    "phoneNumber": "+15551234567"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Contact first name. Example: `Taylor`. |
| `lastName` | string | yes | Contact last name. Example: `Jones`. |
| `email` | string | yes | Contact email address. Example: `taylor@example.com`. |
| `phoneNumber` | string | yes | Contact phone number. Example: `+15551234567`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": {},
      "email": "ava@example.com",
      "first_assistant_id": "string",
      "first_name": "Ava",
      "first_widget_id": "string",
      "id": "string",
      "last_assistant_id": "string",
      "last_name": "Chen",
      "last_seen": "2026-05-07T12:00:00.000Z",
      "last_sent": "2026-05-07T12:00:00.000Z",
      "last_widget_id": "string",
      "org_id": "string",
      "user_attributes": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | object |  |
| `created_at` | date |  |
| `custom_fields` | object |  |
| `email` | string |  |
| `first_assistant_id` | string |  |
| `first_name` | string |  |
| `first_widget_id` | string |  |
| `id` | string |  |
| `last_assistant_id` | string |  |
| `last_name` | string |  |
| `last_seen` | date |  |
| `last_sent` | date |  |
| `last_widget_id` | string |  |
| `org_id` | string |  |
| `user_attributes` | object |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `POST /contact/upsert` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-contact-by-email-or-phone-number.md) for the provider-specific parameters and requirements.

