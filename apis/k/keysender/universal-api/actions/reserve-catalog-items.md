# Keysender: Reserve Catalog Items

Creates a catalog reservation in Keysender.

```
POST https://connect.mindcloud.co/v1/universal/keysender/latest/actions/reserve-catalog-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keysender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/reserve-catalog-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderItems": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keysender/latest/actions/reserve-catalog-items', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderItems": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | no |  |
| `orderItems` | object<object> | yes | Array of reservation line items with sku and quantity. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "orderId": "string",
      "reservationId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Reservation status message. |
| `orderId` | string | Order identifier created for the reservation. |
| `reservationId` | string | Reservation identifier. |
| `status` | string | Reservation status. |

## Native endpoint

Through the native Keysender API, this operation is `POST /catalog/reserve` (base URL `https://panel.keysender.co.uk/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reserve-catalog-items.md) for the provider-specific parameters and requirements.

