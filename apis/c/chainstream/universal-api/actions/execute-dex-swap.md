# Chainstream: Execute DEX Swap

Creates a DEX swap transaction in Chainstream.

```
POST https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/execute-dex-swap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/execute-dex-swap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chain": "string",
  "dex": "string",
  "userAddress": "string",
  "amount": "string",
  "swapMode": "string",
  "slippage": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/execute-dex-swap', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chain": "string",
    "dex": "string",
    "userAddress": "string",
    "amount": "string",
    "swapMode": "string",
    "slippage": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chain` | string | yes | A chain name listed in supported networks |
| `dex` | string | yes | DEX identifier for the trade |
| `userAddress` | string | yes | Public key of the wallet initiating the transaction |
| `amount` | string | yes | Amount to swap |
| `swapMode` | string | yes | Swap direction mode |
| `slippage` | number | yes | Slippage tolerance percentage |
| `inputMint` | string | no | Input token mint address |
| `outputMint` | string | no | Output token mint address |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `priorityFee` | string | no | Priority fee to increase transaction processing speed |
| `poolAddress` | string | no | DEX pool address |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elapsedTime": 1,
      "serializedTx": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `elapsedTime` | number |  |
| `serializedTx` | string |  |

## Native endpoint

Through the native Chainstream API, this operation is `POST /v2/dex/:chain/swap` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-dex-swap.md) for the provider-specific parameters and requirements.

