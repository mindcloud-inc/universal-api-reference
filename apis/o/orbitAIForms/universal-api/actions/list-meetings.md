# Orbit AI (Forms): List Meetings



```
GET https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/list-meetings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orbit AI (Forms) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/list-meetings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/list-meetings?${params}`, {
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
      "attendee_email": "ava@example.com",
      "attendee_name": "Ava Chen",
      "contact_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "end_time": "2026-05-07T12:00:00.000Z",
      "event_type_id": "string",
      "guests": [
        "string"
      ],
      "host_user_id": "string",
      "id": "string",
      "meeting_link": "https://example.com",
      "notes": "string",
      "scheduling_page_id": "string",
      "start_time": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "timezone": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendee_email` | string |  |
| `attendee_name` | string |  |
| `contact_id` | string |  |
| `created_at` | date |  |
| `end_time` | date |  |
| `event_type_id` | string |  |
| `guests` | array<string> |  |
| `host_user_id` | string |  |
| `id` | string |  |
| `meeting_link` | string |  |
| `notes` | string |  |
| `scheduling_page_id` | string |  |
| `start_time` | date |  |
| `status` | string |  |
| `timezone` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Orbit AI (Forms) API, this operation is `GET /api/v1/meetings` (base URL `https://orbitforms.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-meetings.md) for the provider-specific parameters and requirements.

