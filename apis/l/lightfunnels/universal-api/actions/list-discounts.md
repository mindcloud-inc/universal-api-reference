# Lightfunnels: List Discounts



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-discounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-discounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-discounts?${params}`, {
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
      "discounts": {
        "edges": [
          {
            "cursor": "string",
            "node": {
              "id": "string",
              "name": "Ava Chen"
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
| `discounts` | object | Discount connection. |
| `discounts.edges` | array<object> | Discount edges. |
| `discounts.edges[].cursor` | string | Pagination cursor. |
| `discounts.edges[].node` | object | Discount node. |
| `discounts.edges[].node.id` | string | Discount id. |
| `discounts.edges[].node.name` | string | Discount name. |
| `discounts.pageInfo` | object | Pagination info. |
| `discounts.pageInfo.endCursor` | string | Last cursor. |
| `discounts.pageInfo.hasNextPage` | boolean | Whether more discounts exist. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-discounts.md) for the provider-specific parameters and requirements.

