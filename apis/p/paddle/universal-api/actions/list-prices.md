# Paddle: List Prices

Retrieves a list of prices from Paddle.

```
GET https://connect.mindcloud.co/v1/universal/paddle/latest/actions/list-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paddle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paddle/latest/actions/list-prices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paddle/latest/actions/list-prices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Paddle API, this operation is `GET prices` (base URL `https://api.paddle.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-prices.md) for the provider-specific parameters and requirements.

