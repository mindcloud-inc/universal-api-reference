# Chainstream: Get DEX Quote

Retrieves a DEX quote from Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-dex-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-dex-quote?connectionId=$CONNECTION_ID&chain=string&dex=string&amount=string&inputMint=string&outputMint=string&exactIn=true&slippage=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "dex": "string",
  "amount": "string",
  "inputMint": "string",
  "outputMint": "string",
  "exactIn": "true",
  "slippage": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-dex-quote?${params}`, {
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
| `chain` | string | yes | A chain name listed in supported networks |
| `dex` | string | yes | DEX identifier |
| `amount` | string | yes | Amount to quote |
| `inputMint` | string | yes | Input token mint address |
| `outputMint` | string | yes | Output token mint address |
| `exactIn` | boolean | yes | Whether the amount is exact input |
| `slippage` | number | yes | Slippage tolerance percentage |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountOut": "string",
      "currentPrice": "string",
      "executionPrice": "string",
      "fee": "string",
      "minAmountOut": "string",
      "priceImpact": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountOut` | string |  |
| `currentPrice` | string |  |
| `executionPrice` | string |  |
| `fee` | string |  |
| `minAmountOut` | string |  |
| `priceImpact` | string |  |

## Native endpoint

Through the native Chainstream API, this operation is `GET /v2/dex/:chain/quote` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dex-quote.md) for the provider-specific parameters and requirements.

