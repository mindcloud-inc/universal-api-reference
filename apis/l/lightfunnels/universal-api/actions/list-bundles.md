# Lightfunnels: List Bundles



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-bundles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-bundles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-bundles?${params}`, {
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
      "priceBundles": {
        "edges": [
          {
            "cursor": "string",
            "node": {
              "id": "string",
              "label": "string"
            }
          }
        ],
        "pageInfo": {
          "endCursor": "string",
          "hasNextPage": true
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
| `priceBundles` | object | Bundle connection. |
| `priceBundles.edges` | array<object> | Bundle edges. |
| `priceBundles.edges[].cursor` | string | Pagination cursor. |
| `priceBundles.edges[].node` | object | Bundle node. |
| `priceBundles.edges[].node.id` | string | Bundle id. |
| `priceBundles.edges[].node.label` | string | Bundle label. |
| `priceBundles.pageInfo` | object | Pagination info. |
| `priceBundles.pageInfo.endCursor` | string | Last cursor. |
| `priceBundles.pageInfo.hasNextPage` | boolean | Whether more bundles exist. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bundles.md) for the provider-specific parameters and requirements.

