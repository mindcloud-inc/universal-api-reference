# Orbit AI (Forms): Create Scheduling Page Event Type



```
POST https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/create-scheduling-page-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orbit AI (Forms) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/create-scheduling-page-event-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/create-scheduling-page-event-type', {
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
      "buffer_time_after": 1,
      "buffer_time_before": 1,
      "color": "string",
      "duration_minutes": 1,
      "guests_allowed": true,
      "id": "string",
      "is_active": true,
      "location_type": "string",
      "max_booking_days": 1,
      "min_notice_minutes": 1,
      "position": 1,
      "requires_confirmation": true,
      "slug": "string",
      "start_time_increment": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buffer_time_after` | number |  |
| `buffer_time_before` | number |  |
| `color` | string |  |
| `duration_minutes` | number |  |
| `guests_allowed` | boolean |  |
| `id` | string |  |
| `is_active` | boolean |  |
| `location_type` | string |  |
| `max_booking_days` | number |  |
| `min_notice_minutes` | number |  |
| `position` | number |  |
| `requires_confirmation` | boolean |  |
| `slug` | string |  |
| `start_time_increment` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Orbit AI (Forms) API, this operation is `POST /api/v1/scheduling-pages/:id/event-types` (base URL `https://orbitforms.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scheduling-page-event-type.md) for the provider-specific parameters and requirements.

