# ChargeDesk: Create Product

Creates a new product in ChargeDesk.

```
POST https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | Unique product identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "amount_formatted": "string",
      "chargeable": "string",
      "company": "string",
      "currency": "string",
      "description": "string",
      "first_seen": 1,
      "interval": "string",
      "interval_count": "string",
      "name": "Ava Chen",
      "object": "string",
      "product_id": "string",
      "quantity": "string",
      "status": "string",
      "support_url": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `amount_formatted` | string |  |
| `chargeable` | string |  |
| `company` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `first_seen` | number |  |
| `interval` | string |  |
| `interval_count` | string |  |
| `name` | string |  |
| `object` | string |  |
| `product_id` | string |  |
| `quantity` | string |  |
| `status` | string |  |
| `support_url` | string |  |
| `url` | string |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `POST /products` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

