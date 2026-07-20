# Selock: Create Order



```
POST https://connect.mindcloud.co/v1/universal/selock/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/selock/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guest_name": "Ava Chen",
  "guest_phone": "string",
  "start_date": "string",
  "end_date": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/selock/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guest_name": "Ava Chen",
    "guest_phone": "string",
    "start_date": "string",
    "end_date": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guest_name` | string | yes | Guest first name. |
| `guest_surname` | string | no | Guest last name. |
| `guest_phone` | string | yes | Guest phone number. |
| `guest_email` | string | no | Guest email address. |
| `start_date` | string | yes | Check-in date in DD-MM-YYYY format. |
| `hour_in` | number | no | Check-in hour as an integer. |
| `end_date` | string | yes | Check-out date in DD-MM-YYYY format. |
| `hour_out` | number | no | Check-out hour as an integer. |
| `room_id` | number | no | Target room identifier when available. |
| `room_name` | string | no | Target room name when using name-based lookup. |
| `comment` | string | no | Order comment. |
| `price` | number | no | Order price. |
| `paid` | number | no | Amount already paid. |
| `confirmed` | boolean | no | Whether the order is confirmed. |
| `busy` | boolean | no | Whether the order is busy/checked in. |
| `canceled` | boolean | no | Whether the order is canceled. |
| `language` | string | no | Language name from the Selock account. |
| `source` | string | no | Source name from the Selock account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order_id": 1,
      "res": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `order_id` | number | Identifier of the created order. |
| `res` | boolean | True when the order was created. |

## Native endpoint

Through the native Selock API, this operation is `POST /zaiper/create_order/` (base URL `https://selock.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

