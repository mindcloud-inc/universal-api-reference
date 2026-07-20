# Launch27: Create Booking

Creates a new booking in Launch27.

```
POST https://connect.mindcloud.co/v1/universal/launch27/latest/actions/create-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user": {},
  "address": "string",
  "city": "string",
  "state": "string",
  "zip": "string",
  "phone": "string",
  "location_id": 1,
  "frequency_id": 1,
  "service_date": "string",
  "arrival_window": 1,
  "services": {},
  "payment_method": "cash"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/launch27/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user": {},
    "address": "string",
    "city": "string",
    "state": "string",
    "zip": "string",
    "phone": "string",
    "location_id": 1,
    "frequency_id": 1,
    "service_date": "string",
    "arrival_window": 1,
    "services": {},
    "payment_method": "cash"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user` | object | yes | Launch27 booking user object containing first_name, last_name, and email. |
| `address` | string | yes | Booking street address. |
| `city` | string | yes | Booking city. |
| `state` | string | yes | Booking state or region. |
| `zip` | string | yes | Booking postal code. |
| `phone` | string | yes | Booking phone number. |
| `location_id` | number | yes | Launch27 location ID for the booking. |
| `frequency_id` | number | yes | Launch27 frequency ID for the booking. |
| `service_date` | string | yes | Booking service date-time in Launch27 backend format YYYY-MM-DDTHH:mm:ss. |
| `arrival_window` | number | yes | Arrival window in minutes. |
| `services` | list<object> | yes | Selected Launch27 booking services array. |
| `payment_method` | string | yes | Booking payment method such as cash, check, paypal, stripe, or fspay. Default: `cash`. |
| `custom_fields` | list<object> | no | Optional Launch27 booking custom fields array. Default: `[]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Launch27 API returns.

## Native endpoint

Through the native Launch27 API, this operation is `POST booking` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking.md) for the provider-specific parameters and requirements.

