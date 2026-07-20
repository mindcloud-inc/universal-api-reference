# Chainstream: Get Hot Tokens

Retrieves hot tokens from Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-hot-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-hot-tokens?connectionId=$CONNECTION_ID&chain=string&duration=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "duration": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-hot-tokens?${params}`, {
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
| `chain` | string | yes | A chain name listed in supported networks. |
| `duration` | string | yes | Duration of the ranking. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | string | no | Sort field. |
| `sortDirection` | string | no | Sort direction. Default: `desc`. |
| `tag` | string | no | Ranking tag filter. |
| `searchKeywords[]` | array<string> | no | Search keywords. |
| `excludeKeywords[]` | array<string> | no | Exclude keywords. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "address": "string",
          "chain": "string",
          "imageUrl": "https://example.com",
          "marketData": {
            "marketCapInUsd": "string",
            "priceInUsd": "string"
          },
          "name": "Ava Chen",
          "symbol": "string",
          "tokenCreatedAt": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].address` | string |  |
| `data[].chain` | string |  |
| `data[].imageUrl` | string |  |
| `data[].marketData.marketCapInUsd` | string |  |
| `data[].marketData.priceInUsd` | string |  |
| `data[].name` | string |  |
| `data[].symbol` | string |  |
| `data[].tokenCreatedAt` | number |  |

## Native endpoint

Through the native Chainstream API, this operation is `GET /v2/ranking/:chain/hotTokens/:duration` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hot-tokens.md) for the provider-specific parameters and requirements.

