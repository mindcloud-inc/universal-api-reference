# Ventrata: Notify Booking

Sends notifications for a booking in Ventrata.

```
PUT https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/notify-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ventrata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/notify-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/notify-booking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | Booking UUID from Ventrata. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ventrata API returns.

## Native endpoint

Through the native Ventrata API, this operation is `POST octo/bookings/:uuid/notify` (base URL `https://api.ventrata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/notify-booking.md) for the provider-specific parameters and requirements.

