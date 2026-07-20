# Channex: Report Booking No Show

Reports a booking no-show in Channex.

```
PUT https://connect.mindcloud.co/v1/universal/channex/latest/actions/report-booking-no-show
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/channex/latest/actions/report-booking-no-show" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingId": "string",
  "noShowReport": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channex/latest/actions/report-booking-no-show', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookingId": "string",
    "noShowReport": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookingId` | string | yes | UUID of the booking to mark as no-show. |
| `noShowReport` | object | yes | No-show reporting payload object documented by Channex. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.message` | string |  |

## Native endpoint

Through the native Channex API, this operation is `POST /bookings/:bookingId/no_show` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/report-booking-no-show.md) for the provider-specific parameters and requirements.

