# Freshworks CRM: Create Product

Creates a new product in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "product": {},
  "product.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "product": {},
    "product.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `product` | object | yes |  |
| `product.baseCurrencyValue` | number | no |  |
| `product.currencyValue` | number | no |  |
| `product.description` | string | no |  |
| `product.displayName` | string | no |  |
| `product.name` | string | yes |  |
| `product.unitPrice` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "product": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "creater_id": 1,
        "id": 1,
        "is_active": true,
        "is_deleted": true,
        "name": "Ava Chen",
        "pricing_type": 1,
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
| `product.created_at` | date |  |
| `product.creater_id` | number |  |
| `product.id` | number |  |
| `product.is_active` | boolean |  |
| `product.is_deleted` | boolean |  |
| `product.name` | string |  |
| `product.pricing_type` | number |  |
| `product.updated_at` | date |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/cpq/products` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

