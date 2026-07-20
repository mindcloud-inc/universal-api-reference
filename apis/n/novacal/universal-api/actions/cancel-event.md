# Novacal: Cancel Event

Cancels an existing event in Novacal.

```
PUT https://connect.mindcloud.co/v1/universal/novacal/latest/actions/cancel-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novacal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/cancel-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/novacal/latest/actions/cancel-event', {
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
      "canceled_at": "2026-05-07T12:00:00.000Z",
      "cancellation_reason": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canceled_at` | date | Cancellation timestamp. |
| `cancellation_reason` | string | Cancellation reason. |
| `id` | string | Event ID. |
| `status` | string | Event status after cancellation. |

## Native endpoint

Through the native Novacal API, this operation is `PUT /v1/events/:id/cancel` (base URL `https://api.novacal.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-event.md) for the provider-specific parameters and requirements.

