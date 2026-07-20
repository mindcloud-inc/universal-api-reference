# Nautical: List Sales

Retrieves a list of sales from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-sales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-sales?${params}`, {
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
        "sales": {
          "edges": [
            {
              "node": {
                "endDate": "string",
                "id": "string",
                "name": "Ava Chen",
                "startDate": "string",
                "type": "string",
                "value": 1
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
| `data.sales.edges[].node.endDate` | string |  |
| `data.sales.edges[].node.id` | string |  |
| `data.sales.edges[].node.name` | string |  |
| `data.sales.edges[].node.startDate` | string |  |
| `data.sales.edges[].node.type` | string |  |
| `data.sales.edges[].node.value` | number |  |
| `data.sales.pageInfo.endCursor` | string |  |
| `data.sales.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales.md) for the provider-specific parameters and requirements.

