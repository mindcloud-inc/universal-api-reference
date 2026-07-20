# Insighto.ai: Get Contact By Id



```
GET https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/get-contact-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/get-contact-by-id?connectionId=$CONNECTION_ID&contactId=3c90c3cc-0d44-4b50-8888-8dd25736052a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "3c90c3cc-0d44-4b50-8888-8dd25736052a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/get-contact-by-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The UUID id of the contact. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |

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

Through the native Insighto.ai API, this operation is `GET /contact/:contact_id` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-by-id.md) for the provider-specific parameters and requirements.

