# Reloadify: Create Or Update Product

Creates or updates a product in Reloadify.

```
PUT https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageId": "string",
  "product.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageId": "string",
    "product.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageId` | string | yes | Reloadify language ID. |
| `product.brand_id` | string | no | Existing brand ID. |
| `product.name` | string | no | Product name. |
| `product.id` | string | yes | Product identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Reloadify API returns.

## Native endpoint

Through the native Reloadify API, this operation is `PUT /v2/languages/:language_id/products` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-product.md) for the provider-specific parameters and requirements.

