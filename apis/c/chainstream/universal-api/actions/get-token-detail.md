# Chainstream: Get Token Detail

Retrieves token details from Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-token-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-token-detail?connectionId=$CONNECTION_ID&chain=string&tokenAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "tokenAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-token-detail?${params}`, {
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
| `chain` | string | yes | Supported blockchain chain |
| `tokenAddress` | string | yes | Token address |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "chain": "string",
      "decimals": 1,
      "extra": {},
      "imageUrl": "https://example.com",
      "marketData": {},
      "metadataAddress": "string",
      "name": "Ava Chen",
      "socialMedias": {},
      "stats": {},
      "symbol": "string",
      "tokenCreatedAt": 1,
      "tokenCreatedBlockHeight": "string",
      "tokenCreatedSlot": "string",
      "tokenCreatedTxSignature": "string",
      "tokenCreators": [
        {}
      ],
      "uri": "string"
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
| `extra` | object |  |
| `imageUrl` | string |  |
| `marketData` | object |  |
| `metadataAddress` | string |  |
| `name` | string |  |
| `socialMedias` | object |  |
| `stats` | object |  |
| `symbol` | string |  |
| `tokenCreatedAt` | number |  |
| `tokenCreatedBlockHeight` | string |  |
| `tokenCreatedSlot` | string |  |
| `tokenCreatedTxSignature` | string |  |
| `tokenCreators` | array<object> |  |
| `uri` | string |  |

## Native endpoint

Through the native Chainstream API, this operation is `GET /v2/token/:chain/:tokenAddress` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-detail.md) for the provider-specific parameters and requirements.

