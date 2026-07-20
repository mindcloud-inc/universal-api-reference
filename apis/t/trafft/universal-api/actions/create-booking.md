# Trafft: Create Booking

Creates a new booking in Trafft.

```
POST https://connect.mindcloud.co/v1/universal/trafft/latest/actions/create-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trafft `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trafft/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "service": 1,
  "employee": 1,
  "date": "string",
  "time": "string",
  "customer": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trafft/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "service": 1,
    "employee": 1,
    "date": "string",
    "time": "string",
    "customer": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `service` | number | yes | Trafft service ID. |
| `employee` | number | yes | Trafft employee ID. |
| `date` | string | yes | Booking date in YYYY-MM-DD format. |
| `time` | string | yes | Booking start time in HH:mm format. |
| `customer` | number | yes | Trafft customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Trafft API, this operation is `POST /bookings` (base URL `https://mindcloud.admin.trafft.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking.md) for the provider-specific parameters and requirements.

