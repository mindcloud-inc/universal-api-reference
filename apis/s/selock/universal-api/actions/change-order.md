# Selock: Change Order



```
PUT https://connect.mindcloud.co/v1/universal/selock/latest/actions/change-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/selock/latest/actions/change-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "order_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/selock/latest/actions/change-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "order_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order_id` | number | yes | Selock order identifier. |
| `start_date` | string | no | Check-in date in DD-MM-YYYY format. |
| `hour_in` | number | no | Check-in hour as an integer. |
| `end_date` | string | no | Check-out date in DD-MM-YYYY format. |
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
      "res": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `res` | boolean | True when the order change succeeded. |

## Native endpoint

Through the native Selock API, this operation is `POST /zaiper/change_order/` (base URL `https://selock.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-order.md) for the provider-specific parameters and requirements.

