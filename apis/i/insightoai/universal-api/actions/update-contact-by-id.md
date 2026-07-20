# Insighto.ai: Update Contact By Id



```
PUT https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/update-contact-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/update-contact-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "3c90c3cc-0d44-4b50-8888-8dd25736052a"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/update-contact-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "3c90c3cc-0d44-4b50-8888-8dd25736052a"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The UUID id of the contact. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |
| `firstName` | string | no | Contact first name. Example: `Taylor`. |
| `lastName` | string | no | Contact last name. Example: `Jones`. |
| `email` | string | no | Contact email address. Example: `taylor@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": {},
      "custom_fields": {},
      "email": "ava@example.com",
      "first_assistant_id": "string",
      "first_name": "Ava",
      "first_widget_id": "string",
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
| `custom_fields` | object |  |
| `email` | string |  |
| `first_assistant_id` | string |  |
| `first_name` | string |  |
| `first_widget_id` | string |  |
| `last_assistant_id` | string |  |
| `last_name` | string |  |
| `last_seen` | date |  |
| `last_sent` | date |  |
| `last_widget_id` | string |  |
| `org_id` | string |  |
| `user_attributes` | object |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `PUT /contact/:contact_id` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-by-id.md) for the provider-specific parameters and requirements.

