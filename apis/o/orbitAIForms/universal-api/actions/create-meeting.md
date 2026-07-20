# Orbit AI (Forms): Create Meeting



```
POST https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/create-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orbit AI (Forms) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/create-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/create-meeting', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "attendee_email": "ava@example.com",
      "attendee_name": "Ava Chen",
      "attendee_phone": "string",
      "confirmation_email_sent": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "end_time": "2026-05-07T12:00:00.000Z",
      "event_type_id": "string",
      "guests": [
        "string"
      ],
      "id": "string",
      "meeting_link": "https://example.com",
      "notes": "string",
      "scheduling_page_id": "string",
      "start_time": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "timezone": "string"
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
| `attendee_phone` | string |  |
| `confirmation_email_sent` | boolean |  |
| `created_at` | date |  |
| `end_time` | date |  |
| `event_type_id` | string |  |
| `guests` | array<string> |  |
| `id` | string |  |
| `meeting_link` | string |  |
| `notes` | string |  |
| `scheduling_page_id` | string |  |
| `start_time` | date |  |
| `status` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Orbit AI (Forms) API, this operation is `POST /api/calendar/book` (base URL `https://orbitforms.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-meeting.md) for the provider-specific parameters and requirements.

