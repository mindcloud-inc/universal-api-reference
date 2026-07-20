# GetResponse: Upsert Product Categories

Creates or updates product categories for a GetResponse shop product.

```
PUT https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/upsert-product-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/upsert-product-categories" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shopId": "string",
  "productId": "string",
  "categories[]": [
    {}
  ],
  "categories[].categoryId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/upsert-product-categories', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shopId": "string",
    "productId": "string",
    "categories[]": [{}],
    "categories[].categoryId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shopId` | string | yes | The shop ID |
| `productId` | string | yes | The product ID |
| `categories[]` | array<object> | yes | Categories to upsert |
| `categories[].categoryId` | string | yes | Category identifier |
| `categories[].isDefault` | boolean | no | Whether category is default |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GetResponse API returns.

## Native endpoint

Through the native GetResponse API, this operation is `POST /shops/:shopId/products/:productId/categories` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-product-categories.md) for the provider-specific parameters and requirements.

