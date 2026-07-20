# Nautical: List Marketplace Subscriptions

Retrieves a list of marketplace subscriptions from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-marketplace-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-marketplace-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-marketplace-subscriptions?${params}`, {
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
        "marketplaceSubscriptions": {
          "edges": [
            {
              "node": {
                "id": "string",
                "isActive": true,
                "provider": "string",
                "providerCustomerId": "string"
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
| `data.marketplaceSubscriptions.edges[].node.id` | string |  |
| `data.marketplaceSubscriptions.edges[].node.isActive` | boolean |  |
| `data.marketplaceSubscriptions.edges[].node.provider` | string |  |
| `data.marketplaceSubscriptions.edges[].node.providerCustomerId` | string |  |
| `data.marketplaceSubscriptions.pageInfo.endCursor` | string |  |
| `data.marketplaceSubscriptions.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-marketplace-subscriptions.md) for the provider-specific parameters and requirements.

