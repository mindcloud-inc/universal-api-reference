# Tidio: Upsert Products

Upserts products in the Tidio product catalog.

```
PUT https://connect.mindcloud.co/v1/universal/tidio/latest/actions/upsert-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/upsert-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "products": {},
  "products[].id": 1,
  "products[].url": "https://example.com",
  "products[].title": "string",
  "products[].description": "string",
  "products[].defaultCurrency": "string",
  "products[].status": "string",
  "products[].price": 1,
  "products[].features": {},
  "products[].updatedAt": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidio/latest/actions/upsert-products', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "products": {},
    "products[].id": 1,
    "products[].url": "https://example.com",
    "products[].title": "string",
    "products[].description": "string",
    "products[].defaultCurrency": "string",
    "products[].status": "string",
    "products[].price": 1,
    "products[].features": {},
    "products[].updatedAt": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `products` | list<object> | yes | List of products to upsert. Maximum 100 products per request. |
| `products[].id` | number | yes | Unique identifier for the product. |
| `products[].url` | string | yes | Direct URL of the product. |
| `products[].imageUrl` | string | no | Default image URL of the product. |
| `products[].title` | string | yes | Title of the product. |
| `products[].description` | string | yes | Product description. |
| `products[].defaultCurrency` | string | yes | Default currency code for the product. |
| `products[].vendor` | string | no | Brand or supplier of the product. |
| `products[].productType` | string | no | Category or type of product. |
| `products[].status` | string | yes | Determines if the product should be recommended by Lyro. |
| `products[].price` | number | yes | Product price. |
| `products[].sku` | string | no | Stock Keeping Unit identifier. |
| `products[].barcode` | string | no | Barcode of the product. |
| `products[].features` | object | yes | Key-value dictionary for product features and configurable options. |
| `products[].updatedAt` | date | yes | Last update timestamp in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. Tidio docs specify 204 Request succeeded but no content returned. |

## Native endpoint

Through the native Tidio API, this operation is `PUT /products/batch` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-products.md) for the provider-specific parameters and requirements.

