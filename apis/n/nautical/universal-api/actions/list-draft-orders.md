# Nautical: List Draft Orders

Retrieves a list of draft orders from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-draft-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-draft-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-draft-orders?${params}`, {
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
        "draftOrders": {
          "edges": [
            {
              "node": {
                "created": "string",
                "id": "string",
                "status": "string",
                "updated": "string"
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
| `data.draftOrders.edges[].node.created` | string |  |
| `data.draftOrders.edges[].node.id` | string |  |
| `data.draftOrders.edges[].node.status` | string |  |
| `data.draftOrders.edges[].node.updated` | string |  |
| `data.draftOrders.pageInfo.endCursor` | string |  |
| `data.draftOrders.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-draft-orders.md) for the provider-specific parameters and requirements.

