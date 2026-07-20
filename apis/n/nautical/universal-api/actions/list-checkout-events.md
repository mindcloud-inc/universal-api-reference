# Nautical: List Checkout Events

Retrieves a list of checkout events from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-checkout-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-checkout-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-checkout-events?${params}`, {
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
        "checkoutEvents": {
          "edges": [
            {
              "node": {
                "checkoutId": "string",
                "createdAt": "string",
                "id": "string",
                "type": "string"
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
| `data.checkoutEvents.edges[].node.checkoutId` | string |  |
| `data.checkoutEvents.edges[].node.createdAt` | string |  |
| `data.checkoutEvents.edges[].node.id` | string |  |
| `data.checkoutEvents.edges[].node.type` | string |  |
| `data.checkoutEvents.pageInfo.endCursor` | string |  |
| `data.checkoutEvents.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-checkout-events.md) for the provider-specific parameters and requirements.

