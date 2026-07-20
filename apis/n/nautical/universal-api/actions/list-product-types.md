# Nautical: List Product Types

Retrieves a list of product types from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-product-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-product-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-product-types?${params}`, {
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
        "productTypes": {
          "edges": [
            {
              "node": {
                "id": "string",
                "isDigital": true,
                "name": "Ava Chen",
                "slug": "string"
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
| `data.productTypes.edges[].node.id` | string |  |
| `data.productTypes.edges[].node.isDigital` | boolean |  |
| `data.productTypes.edges[].node.name` | string |  |
| `data.productTypes.edges[].node.slug` | string |  |
| `data.productTypes.pageInfo.endCursor` | string |  |
| `data.productTypes.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-product-types.md) for the provider-specific parameters and requirements.

