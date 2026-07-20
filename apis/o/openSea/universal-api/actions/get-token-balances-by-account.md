# OpenSea: Get Token Balances By Wallet

Retrieves token balances for an OpenSea account.

```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-token-balances-by-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-token-balances-by-account?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-token-balances-by-account?${params}`, {
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
| `address` | string | yes | Wallet address |
| `limit` | number | no | Number of results to return (default: 20, max: 25) |
| `chains[]` | array<string> | no | Filter by blockchain(s) Accepts multiple values in one string, delimited by `,`. |
| `sortBy` | string | no | Sort field (default: usd_value) |
| `sortDirection` | string | no | Sort direction (default: desc) |
| `disableSpamFiltering` | boolean | no | Disable spam token filtering (default: false) |
| `cursor` | string | no | Pagination cursor for next page |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native OpenSea API, this operation is `GET /api/v2/account/{address}/tokens` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-balances-by-account.md) for the provider-specific parameters and requirements.

