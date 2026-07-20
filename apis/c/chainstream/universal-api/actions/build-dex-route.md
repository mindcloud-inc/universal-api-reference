# Chainstream: Build DEX Route

Calculates the best DEX swap route in Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/build-dex-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/build-dex-route?connectionId=$CONNECTION_ID&chain=string&dex=string&userAddress=string&amount=string&swapMode=string&slippage=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "dex": "string",
  "userAddress": "string",
  "amount": "string",
  "swapMode": "string",
  "slippage": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/build-dex-route?${params}`, {
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
| `recipientAddress` | string | no | Recipient wallet address for the swap |
| `permit` | string | no | Permit data for the swap |
| `deadline` | number | no | Swap deadline timestamp |
| `tipFee` | string | no | Tip fee to increase transaction processing speed |
| `isAntiMev` | boolean | no | Whether to enable anti-MEV protection |
| `maxFeePerGas` | string | no | Maximum fee per gas unit in wei |
| `maxPriorityFeePerGas` | string | no | Maximum priority fee per gas unit in wei |
| `gasPrice` | string | no | Gas price in wei |
| `gasLimit` | string | no | Gas limit for the transaction |

## Response

```json
{
  "success": true,
  "data": [
    {
      "args": {
        "amount": "string",
        "dex": "string",
        "inputMint": "string",
        "outputMint": "string",
        "slippage": 1,
        "swapMode": "string",
        "userAddress": "string"
      },
      "elapsedTime": 1,
      "routeInfo": {
        "contextSlot": 1,
        "inAmount": "string",
        "inputMint": "string",
        "otherAmountThreshold": "string",
        "outAmount": "string",
        "outputMint": "string",
        "routePlan": [
          {
            "percent": 1,
            "swapInfo": {
              "ammKey": "string",
              "label": "string"
            }
          }
        ],
        "slippageBps": 1,
        "swapMode": "string",
        "timeTaken": 1
      },
      "serializedTx": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `args.amount` | string |  |
| `args.dex` | string |  |
| `args.inputMint` | string |  |
| `args.outputMint` | string |  |
| `args.slippage` | number |  |
| `args.swapMode` | string |  |
| `args.userAddress` | string |  |
| `elapsedTime` | number |  |
| `routeInfo.contextSlot` | number |  |
| `routeInfo.inAmount` | string |  |
| `routeInfo.inputMint` | string |  |
| `routeInfo.otherAmountThreshold` | string |  |
| `routeInfo.outAmount` | string |  |
| `routeInfo.outputMint` | string |  |
| `routeInfo.routePlan[].percent` | number |  |
| `routeInfo.routePlan[].swapInfo.ammKey` | string |  |
| `routeInfo.routePlan[].swapInfo.label` | string |  |
| `routeInfo.slippageBps` | number |  |
| `routeInfo.swapMode` | string |  |
| `routeInfo.timeTaken` | number |  |
| `serializedTx` | string |  |

## Native endpoint

Through the native Chainstream API, this operation is `POST /v2/dex/:chain/route` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/build-dex-route.md) for the provider-specific parameters and requirements.

