# Lodgify: Update Reservation Status

Updates a booking's status in Lodgify.

```
PUT https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/update-reservation-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lodgify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/update-reservation-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reservationId": "19199854",
  "statusAction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/update-reservation-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reservationId": "19199854",
    "statusAction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reservationId` | number | yes | Reservation identifier from Lodgify. Example: `19199854`. |
| `statusAction` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Lodgify API returns.

## Native endpoint

Through the native Lodgify API, this operation is `PUT /v1/reservation/booking/:id/:statusAction` (base URL `https://api.lodgify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reservation-status.md) for the provider-specific parameters and requirements.

