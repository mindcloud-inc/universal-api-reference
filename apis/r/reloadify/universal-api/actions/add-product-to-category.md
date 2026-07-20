# Reloadify: Add Product To Category

Adds a product to a category in Reloadify.

```
PUT https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/add-product-to-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/add-product-to-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "language_id": "string",
  "product_id": "string",
  "category_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/add-product-to-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "language_id": "string",
    "product_id": "string",
    "category_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_id` | string | yes | Language ID from the Reloadify language resource. |
| `product_id` | string | yes | Product ID. |
| `category_id` | string | yes | Category ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": 1,
      "productId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number |  |
| `productId` | number |  |

## Native endpoint

Through the native Reloadify API, this operation is `PUT /v2/languages/:language_id/products/:product_id/categories/:category_id` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-product-to-category.md) for the provider-specific parameters and requirements.

