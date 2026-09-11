# BigCommerce: Get Product Metafield



```
GET https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/get-product-metafield
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/get-product-metafield?connectionId=$CONNECTION_ID&productId=string&metafieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string",
  "metafieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/get-product-metafield?${params}`, {
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
| `productId` | string | yes |  |
| `metafieldId` | string | yes |  |
| `includeFields[]` | array | no |  |
| `excludeFields[]` | array | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `GET /v3/catalog/products/:productId/metafields/:metafieldId` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-metafield.md) for the provider-specific parameters and requirements.

