# Lome: List Recent Responses

Retrieves sign up form responses from the last 24 hours in Lome.

```
GET https://connect.mindcloud.co/v1/universal/lome/latest/actions/list-recent-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lome/latest/actions/list-recent-responses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lome/latest/actions/list-recent-responses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "community": "string",
      "contact_email": "ava@example.com",
      "contact_name": "Ava Chen",
      "contact_phone": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "event_id": "string",
      "event_link": "https://example.com",
      "event_title": "string",
      "id": "string",
      "response_custom_fields": {},
      "response_date": "2026-05-07T12:00:00.000Z",
      "response_end_time": "2026-05-07T12:00:00.000Z",
      "response_formatted": "string",
      "response_group": "string",
      "response_item": "string",
      "response_message": "string",
      "response_number": 1,
      "response_start_time": "2026-05-07T12:00:00.000Z",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `community` | string |  |
| `contact_email` | string |  |
| `contact_name` | string |  |
| `contact_phone` | string |  |
| `created_at` | date |  |
| `event_id` | string |  |
| `event_link` | string |  |
| `event_title` | string |  |
| `id` | string |  |
| `response_custom_fields` | object |  |
| `response_date` | date |  |
| `response_end_time` | date |  |
| `response_formatted` | string |  |
| `response_group` | string |  |
| `response_item` | string |  |
| `response_message` | string |  |
| `response_number` | number |  |
| `response_start_time` | date |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Lome API, this operation is `GET /v1/webhook/new-response/recent` (base URL `https://grow.withlome.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-responses.md) for the provider-specific parameters and requirements.

