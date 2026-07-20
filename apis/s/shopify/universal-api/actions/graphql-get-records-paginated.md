# Shopify: GraphQL - Get Records (Paginated)

Retrieves records from Shopify with paginated GraphQL queries.

```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/graphql-get-records-paginated
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/graphql-get-records-paginated?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/graphql-get-records-paginated?${params}`, {
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
| `query` | string | no |  |
| `variables` | object | no |  |
| `version` | string | no | Default: `2024-04`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "orders": {
          "edges": [
            {
              "node": {
                "id": "string"
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
| `data.orders.edges[].node.id` | string |  |
| `data.orders.pageInfo.endCursor` | string |  |
| `data.orders.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Shopify API, this operation is `POST :version/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/graphql-get-records-paginated.md) for the provider-specific parameters and requirements.

