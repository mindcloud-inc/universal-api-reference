# Eventee: Update Lecture

Updates an existing lecture in Eventee.

```
PUT https://connect.mindcloud.co/v1/universal/eventee/latest/actions/update-lecture
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/update-lecture" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventee/latest/actions/update-lecture', {
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
      "booking_info": [
        {}
      ],
      "capacity": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "discussion": true,
      "end": "2026-05-07T12:00:00.000Z",
      "hall_id": 1,
      "id": 1,
      "moderating": true,
      "name": "Ava Chen",
      "polling": true,
      "speakers": [
        "string"
      ],
      "start": "2026-05-07T12:00:00.000Z",
      "stream": {},
      "tracks": [
        "string"
      ],
      "type": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "virtual_meeting": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `booking_info` | array<object> |  |
| `capacity` | number |  |
| `created_at` | date |  |
| `description` | string |  |
| `discussion` | boolean |  |
| `end` | date |  |
| `hall_id` | number |  |
| `id` | number |  |
| `moderating` | boolean |  |
| `name` | string |  |
| `polling` | boolean |  |
| `speakers` | array |  |
| `start` | date |  |
| `stream` | object |  |
| `tracks` | array |  |
| `type` | number |  |
| `updated_at` | date |  |
| `virtual_meeting` | object |  |

## Native endpoint

Through the native Eventee API, this operation is `PATCH /lecture/{id}` (base URL `https://api.eventee.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lecture.md) for the provider-specific parameters and requirements.

