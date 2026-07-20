# Freshworks CRM: Get Related Products

Retrieves related products from Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-related-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-related-products?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-related-products?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "products": [
        {
          "base_currency_amount": 1,
          "category": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "creater_id": 1,
          "description": "string",
          "id": 1,
          "is_active": true,
          "is_deleted": true,
          "name": "Ava Chen",
          "owner_id": 1,
          "pricing_type": 1,
          "sku_number": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "updater_id": 1,
          "valid_till": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `products[].base_currency_amount` | number |  |
| `products[].category` | string |  |
| `products[].created_at` | date |  |
| `products[].creater_id` | number |  |
| `products[].description` | string |  |
| `products[].id` | number |  |
| `products[].is_active` | boolean |  |
| `products[].is_deleted` | boolean |  |
| `products[].name` | string |  |
| `products[].owner_id` | number |  |
| `products[].pricing_type` | number |  |
| `products[].sku_number` | string |  |
| `products[].updated_at` | date |  |
| `products[].updater_id` | number |  |
| `products[].valid_till` | date |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET /api/cpq/cpq_documents/:id/related_products` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-related-products.md) for the provider-specific parameters and requirements.

