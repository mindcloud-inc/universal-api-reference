# Nautical: List Checkout Lines

Retrieves a list of checkout lines from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-checkout-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-checkout-lines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-checkout-lines?${params}`, {
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
        "checkoutLines": {
          "edges": [
            {
              "node": {
                "id": "string",
                "note": "string",
                "quantity": 1
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
| `data.checkoutLines.edges[].node.id` | string |  |
| `data.checkoutLines.edges[].node.note` | string |  |
| `data.checkoutLines.edges[].node.quantity` | number |  |
| `data.checkoutLines.pageInfo.endCursor` | string |  |
| `data.checkoutLines.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-checkout-lines.md) for the provider-specific parameters and requirements.

