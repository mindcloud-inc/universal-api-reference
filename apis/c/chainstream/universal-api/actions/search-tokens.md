# Chainstream: Search Tokens

Finds tokens in Chainstream by search query.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/search-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/search-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/search-tokens?${params}`, {
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
| `chains` | string | no | Chain filter |
| `cursor` | string | no | Pagination cursor |
| `direction` | string | no | Pagination direction |
| `limit` | string | no | Number of results per page |
| `mode` | string | no | Search mode |
| `protocols` | string | no | Protocol filter |
| `q` | string | no | Search query string for token name, symbol, or address |
| `sort` | string | no | Sort direction |
| `sortBy` | string | no | Field to sort by |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "chain": "string",
      "decimals": 1,
      "imageUrl": "https://example.com",
      "marketData": {},
      "name": "Ava Chen",
      "socialMedias": {},
      "stats": {},
      "symbol": "string",
      "tokenCreatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `chain` | string |  |
| `decimals` | number |  |
| `imageUrl` | string |  |
| `marketData` | object |  |
| `name` | string |  |
| `socialMedias` | object |  |
| `stats` | object |  |
| `symbol` | string |  |
| `tokenCreatedAt` | number |  |

## Native endpoint

Through the native Chainstream API, this operation is `GET /v2/token/search` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tokens.md) for the provider-specific parameters and requirements.

