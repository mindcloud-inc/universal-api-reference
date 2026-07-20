# Freshworks CRM: Manage Product Prices

Updates product prices in Freshworks CRM.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/manage-product-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/manage-product-prices" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "product": {},
  "product.product_pricings[]": [
    {}
  ],
  "product.product_pricings[].currency_code": "string",
  "product.product_pricings[].currency_value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/manage-product-prices', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "product": {},
    "product.product_pricings[]": [{}],
    "product.product_pricings[].currency_code": "string",
    "product.product_pricings[].currency_value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `product` | object | yes |  |
| `product.product_pricings[]` | array<object> | yes |  |
| `product.product_pricings[].currency_code` | string | yes |  |
| `product.product_pricings[].currency_value` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "product": {
        "base_currency_amount": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "creater_id": 1,
        "id": 1,
        "is_active": true,
        "is_deleted": true,
        "name": "Ava Chen",
        "owner_id": 1,
        "pricing_type": 1,
        "product_pricings": [
          {
            "_destroy": true,
            "currency_code": "string",
            "id": 1,
            "is_locked": true,
            "setup_fee": 1,
            "unit_price": 1
          }
        ],
        "updated_at": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `product.base_currency_amount` | number |  |
| `product.created_at` | date |  |
| `product.creater_id` | number |  |
| `product.id` | number |  |
| `product.is_active` | boolean |  |
| `product.is_deleted` | boolean |  |
| `product.name` | string |  |
| `product.owner_id` | number |  |
| `product.pricing_type` | number |  |
| `product.product_pricings[]._destroy` | boolean |  |
| `product.product_pricings[].currency_code` | string |  |
| `product.product_pricings[].id` | number |  |
| `product.product_pricings[].is_locked` | boolean |  |
| `product.product_pricings[].setup_fee` | number |  |
| `product.product_pricings[].unit_price` | number |  |
| `product.updated_at` | date |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `PUT /api/cpq/products/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/manage-product-prices.md) for the provider-specific parameters and requirements.

