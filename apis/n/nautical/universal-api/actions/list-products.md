# Nautical: List Products

Retrieves a list of products from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-products?${params}`, {
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
        "products": {
          "edges": [
            {
              "node": {
                "externalId": "string",
                "id": "string",
                "name": "Ava Chen",
                "publicationDate": "string",
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
| `data.products.edges[].node.externalId` | string |  |
| `data.products.edges[].node.id` | string |  |
| `data.products.edges[].node.name` | string |  |
| `data.products.edges[].node.publicationDate` | string |  |
| `data.products.edges[].node.slug` | string |  |
| `data.products.pageInfo.endCursor` | string |  |
| `data.products.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

