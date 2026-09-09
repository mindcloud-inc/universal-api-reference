# Walmart: Get Token Detail

Returns OAuth token metadata and scopes granted by the seller to your application. Use this to verify whether a token is valid, when it expires, and which API categories are allowed (full_access, view_only, no_access).

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-token-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-token-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-token-detail?${params}`, {
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
      "expireAt": "string",
      "isChannelMatch": true,
      "issuedAt": "string",
      "isValid": true,
      "scopes": {
        "content": "string",
        "feeds": "string",
        "fulfillment": "string",
        "inventory": "string",
        "item": "string",
        "lagtime": "string",
        "orders": "string",
        "price": "string",
        "profile": "string",
        "promo": "string",
        "report": "string",
        "reports": "string",
        "repricer": "string",
        "returns": "string",
        "rules": "string",
        "shipping": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expireAt` | string |  |
| `isChannelMatch` | boolean |  |
| `issuedAt` | string |  |
| `isValid` | boolean |  |
| `scopes.content` | string |  |
| `scopes.feeds` | string |  |
| `scopes.fulfillment` | string |  |
| `scopes.inventory` | string |  |
| `scopes.item` | string |  |
| `scopes.lagtime` | string |  |
| `scopes.orders` | string |  |
| `scopes.price` | string |  |
| `scopes.profile` | string |  |
| `scopes.promo` | string |  |
| `scopes.report` | string |  |
| `scopes.reports` | string |  |
| `scopes.repricer` | string |  |
| `scopes.returns` | string |  |
| `scopes.rules` | string |  |
| `scopes.shipping` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/token/detail` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-detail.md) for the provider-specific parameters and requirements.

