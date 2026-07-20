# Goody: Calculate Order Batch Price

Calculates an order batch price in Goody.

```
GET https://connect.mindcloud.co/v1/universal/goody/latest/actions/calculate-order-batch-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goody `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goody/latest/actions/calculate-order-batch-price?connectionId=$CONNECTION_ID&recipients%5B%5D=%5Bobject%20Object%5D&cart=%5Bobject%20Object%5D&sendMethod=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recipients[]": "[object Object]",
  "cart": "[object Object]",
  "sendMethod": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goody/latest/actions/calculate-order-batch-price?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipients[]` | array<object> | yes |  |
| `cart` | object | yes |  |
| `sendMethod` | string | yes | The method for sending a order batch. `email_and_link` sends a gift email to the recipient (specify `email` for each recipient). `link_multiple_custom_list` generates a gift link without an automatic email. `direct_send` ships the product directly to the recipient (specify `mailing_address` for each recipient). For more information, see [Send Methods](/introduction/send-methods). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cart_price": {
        "price_est_tax_high": 1,
        "price_est_tax_low": 1,
        "price_est_total_high": 1,
        "price_est_total_low": 1,
        "price_pre_tax": 1,
        "price_processing_fee": 1,
        "price_product": 1,
        "price_shipping": 1
      },
      "total_price": {
        "est_group_total_high": 1,
        "est_group_total_low": 1,
        "recipients": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cart_price` | object |  |
| `cart_price.price_est_tax_high` | number |  |
| `cart_price.price_est_tax_low` | number |  |
| `cart_price.price_est_total_high` | number |  |
| `cart_price.price_est_total_low` | number |  |
| `cart_price.price_pre_tax` | number |  |
| `cart_price.price_processing_fee` | number |  |
| `cart_price.price_product` | number |  |
| `cart_price.price_shipping` | number |  |
| `total_price` | object |  |
| `total_price.est_group_total_high` | number |  |
| `total_price.est_group_total_low` | number |  |
| `total_price.recipients` | number |  |

## Native endpoint

Through the native Goody API, this operation is `POST /v1/order_batches/price` (base URL `https://api.ongoody.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-order-batch-price.md) for the provider-specific parameters and requirements.

