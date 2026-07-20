# Nautical: List Refunds

Retrieves a list of refunds from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-refunds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-refunds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-refunds?${params}`, {
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
        "refunds": {
          "edges": [
            {
              "node": {
                "createdAt": "string",
                "description": "string",
                "id": "string",
                "name": "Ava Chen",
                "updatedAt": "string"
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
| `data.refunds.edges[].node.createdAt` | string |  |
| `data.refunds.edges[].node.description` | string |  |
| `data.refunds.edges[].node.id` | string |  |
| `data.refunds.edges[].node.name` | string |  |
| `data.refunds.edges[].node.updatedAt` | string |  |
| `data.refunds.pageInfo.endCursor` | string |  |
| `data.refunds.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-refunds.md) for the provider-specific parameters and requirements.

