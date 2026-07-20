# Understory: Create Booking

Creates a new booking in Understory.

```
POST https://connect.mindcloud.co/v1/universal/understory/latest/actions/create-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/understory/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string",
  "customer": {},
  "locale": "string",
  "items": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/understory/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string",
    "customer": {},
    "locale": "string",
    "items": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | The unique identifier of the event. |
| `customer` | object | yes | The customer making the booking as a structured object. |
| `locale` | string | yes | A lowercase ISO 639-1 language code, optionally with country suffix like en-US. |
| `items` | list<object> | yes | One or more booking items as a list of objects. |
| `metadata` | object | no | Optional custom metadata object for the booking. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Understory API, this operation is `POST /v1/bookings` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking.md) for the provider-specific parameters and requirements.

