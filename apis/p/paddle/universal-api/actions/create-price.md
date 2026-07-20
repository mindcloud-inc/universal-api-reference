# Paddle: Create Price

Creates a new price in Paddle.

```
POST https://connect.mindcloud.co/v1/universal/paddle/latest/actions/create-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paddle/latest/actions/create-price" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paddle/latest/actions/create-price', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "billing_cycle": {
        "frequency": 1,
        "interval": "string"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "product_id": "string",
      "quantity": {
        "maximum": 1,
        "minimum": 1
      },
      "status": "string",
      "tax_mode": "string",
      "trial_period": {
        "frequency": 1,
        "interval": "string",
        "requires_payment_method": true
      },
      "type": "string",
      "unit_price": {
        "amount": "string",
        "currency_code": "string"
      },
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing_cycle.frequency` | number |  |
| `billing_cycle.interval` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `product_id` | string |  |
| `quantity.maximum` | number |  |
| `quantity.minimum` | number |  |
| `status` | string |  |
| `tax_mode` | string |  |
| `trial_period.frequency` | number |  |
| `trial_period.interval` | string |  |
| `trial_period.requires_payment_method` | boolean |  |
| `type` | string |  |
| `unit_price.amount` | string |  |
| `unit_price.currency_code` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Paddle API, this operation is `POST prices` (base URL `https://api.paddle.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-price.md) for the provider-specific parameters and requirements.

