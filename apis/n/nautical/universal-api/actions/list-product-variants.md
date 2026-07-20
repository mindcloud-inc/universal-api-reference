# Nautical: List Product Variants

Retrieves a list of product variants from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-product-variants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-product-variants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-product-variants?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "productVariants": {
          "edges": [
            {
              "node": {
                "id": "string",
                "name": "Ava Chen",
                "nauticalStockNumber": "string",
                "sku": "string",
                "status": "string"
              }
            }
          ],
          "pageInfo": {
            "endCursor": "string",
            "hasNextPage": true
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.productVariants.edges[].node.id` | string |  |
| `data.productVariants.edges[].node.name` | string |  |
| `data.productVariants.edges[].node.nauticalStockNumber` | string |  |
| `data.productVariants.edges[].node.sku` | string |  |
| `data.productVariants.edges[].node.status` | string |  |
| `data.productVariants.pageInfo.endCursor` | string |  |
| `data.productVariants.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-product-variants.md) for the provider-specific parameters and requirements.

