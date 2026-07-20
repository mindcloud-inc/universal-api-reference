# Novacal: Update Event Type

Updates an existing event type in Novacal.

```
PUT https://connect.mindcloud.co/v1/universal/novacal/latest/actions/update-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novacal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/update-event-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/novacal/latest/actions/update-event-type', {
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
      "color": "string",
      "duration": 1,
      "hidden_from_profile": true,
      "id": 1,
      "name": "Ava Chen",
      "slug": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Event type color. |
| `duration` | number | Duration in minutes. |
| `hidden_from_profile` | boolean | Whether the event type is hidden from the profile. |
| `id` | number | Event type ID. |
| `name` | string | Event type name. |
| `slug` | string | Event type slug. |
| `type` | string | Event type scheduling mode. |

## Native endpoint

Through the native Novacal API, this operation is `PUT /v1/event-types/:id` (base URL `https://api.novacal.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event-type.md) for the provider-specific parameters and requirements.

