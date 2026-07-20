# Eventee: Update Attendee Check-In

Updates attendee check-in status in Eventee.

```
PUT https://connect.mindcloud.co/v1/universal/eventee/latest/actions/update-attendee-check-in
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/update-attendee-check-in" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventee/latest/actions/update-attendee-check-in', {
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
      "checked_at": "2026-05-07T12:00:00.000Z",
      "company": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "group_id": 1,
      "id": 1,
      "last_name": "Chen",
      "name": "Ava Chen",
      "position": "string",
      "registered_at": "2026-05-07T12:00:00.000Z",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checked_at` | date |  |
| `company` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `group_id` | number |  |
| `id` | number |  |
| `last_name` | string |  |
| `name` | string |  |
| `position` | string |  |
| `registered_at` | date |  |
| `role` | string |  |

## Native endpoint

Through the native Eventee API, this operation is `PUT /attendee/{id}/checkin` (base URL `https://api.eventee.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-attendee-check-in.md) for the provider-specific parameters and requirements.

