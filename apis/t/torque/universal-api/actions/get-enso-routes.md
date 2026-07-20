# Torque: Get Enso Routes



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-enso-routes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-enso-routes?connectionId=$CONNECTION_ID&fromAddress=string&tokenIn=string&tokenOut=string&amountIn=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromAddress": "string",
  "tokenIn": "string",
  "tokenOut": "string",
  "amountIn": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-enso-routes?${params}`, {
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
| `fromAddress` | string | yes | Wallet address requesting the route. |
| `chainId` | number | no | Blockchain chain ID. Defaults to Ethereum mainnet when Torque provides a default. |
| `tokenIn` | string | yes | Input token address or addresses. |
| `tokenOut` | string | yes | Output token address or addresses. |
| `amountIn` | string | yes | Input amount or amounts in wei. |
| `slippage` | string | no | Slippage in basis points. Torque defaults to 50. |
| `routingStrategy` | list | no | Routing strategy. Torque defaults to delegate. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bestRoute": {},
      "gasEstimate": "string",
      "inputAmount": "string",
      "minimumReceived": "string",
      "outputAmount": "string",
      "priceImpact": 1,
      "route": {},
      "routes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bestRoute` | object |  |
| `gasEstimate` | string |  |
| `inputAmount` | string |  |
| `minimumReceived` | string |  |
| `outputAmount` | string |  |
| `priceImpact` | number |  |
| `route` | object |  |
| `routes` | array<object> |  |

## Native endpoint

Through the native Torque API, this operation is `POST /enso/routes` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enso-routes.md) for the provider-specific parameters and requirements.

