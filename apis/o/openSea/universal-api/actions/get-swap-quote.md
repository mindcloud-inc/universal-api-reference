# OpenSea: Get Swap Quote

Retrieves a swap quote from OpenSea.

```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-swap-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-swap-quote?connectionId=$CONNECTION_ID&fromChain=string&fromAddress=string&toChain=string&toAddress=string&quantity=string&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromChain": "string",
  "fromAddress": "string",
  "toChain": "string",
  "toAddress": "string",
  "quantity": "string",
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-swap-quote?${params}`, {
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
| `fromChain` | string | yes | Chain of the token to swap from |
| `fromAddress` | string | yes | Contract address of the token to swap from |
| `toChain` | string | yes | Chain of the token to swap to |
| `toAddress` | string | yes | Contract address of the token to swap to |
| `quantity` | string | yes | Amount to swap in the smallest unit of the token (e.g. wei for ETH) |
| `address` | string | yes | Wallet address executing the swap |
| `slippage` | number | no | Slippage tolerance (0.0 to 0.5, default: 0.01) |
| `recipient` | string | no | Recipient address (defaults to sender address) |

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

Through the native OpenSea API, this operation is `GET /api/v2/swap/quote` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-swap-quote.md) for the provider-specific parameters and requirements.

