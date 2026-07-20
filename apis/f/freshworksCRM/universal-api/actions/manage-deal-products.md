# Freshworks CRM: Manage Deal Products

Updates products on a deal in Freshworks CRM.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/manage-deal-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/manage-deal-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/manage-deal-products', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `products[]` | array<object> | no |  |
| `products[].id` | number | no |  |
| `products[].quantity` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deal": {
        "amount": "string",
        "base_currency_amount": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "has_products": true,
        "id": 1,
        "name": "Ava Chen",
        "products": [
          [
            {}
          ]
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
| `deal` | object |  |
| `deal.amount` | string |  |
| `deal.base_currency_amount` | string |  |
| `deal.created_at` | date |  |
| `deal.has_products` | boolean |  |
| `deal.id` | number |  |
| `deal.name` | string |  |
| `deal.products[]` | array<object> |  |
| `deal.updated_at` | date |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `PUT /api/deals/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/manage-deal-products.md) for the provider-specific parameters and requirements.

