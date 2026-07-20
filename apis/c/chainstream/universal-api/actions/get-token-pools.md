# Chainstream: Get Token Pools

Retrieves token pools from Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-token-pools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-token-pools?connectionId=$CONNECTION_ID&chain=string&tokenAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "tokenAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-token-pools?${params}`, {
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
| `tokenAddress` | string | yes | Token contract address |
| `cursor` | string | no | Pagination cursor |
| `limit` | string | no | Number of results per page |
| `direction` | string | no | Pagination direction |
| `sortBy` | string | no | Pool sort field |
| `sortDirection` | string | no | Sort direction |
| `minTvlInSol` | string | no | Minimum TVL in SOL |
| `maxTvlInSol` | string | no | Maximum TVL in SOL |
| `minTvlInUsd` | string | no | Minimum TVL in USD |
| `maxTvlInUsd` | string | no | Maximum TVL in USD |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chain": "string",
      "poolAddress": "string",
      "programAddress": "string",
      "tokenAAddress": "string",
      "tokenBAddress": "string",
      "tvlInSol": "string",
      "tvlInUsd": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chain` | string |  |
| `poolAddress` | string |  |
| `programAddress` | string |  |
| `tokenAAddress` | string |  |
| `tokenBAddress` | string |  |
| `tvlInSol` | string |  |
| `tvlInUsd` | string |  |

## Native endpoint

Through the native Chainstream API, this operation is `GET /v2/token/:chain/:tokenAddress/pools` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-pools.md) for the provider-specific parameters and requirements.

