# Get Enso Routes with Torque

## Endpoint

- **Method:** `POST`
- **Path:** `/enso/routes`
- **Base URL:** `https://app.torque.fi/api`
- **Official documentation:** [Get Enso Routes](https://docs.torque.fi/business/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromAddress` | body | `string` | yes | Wallet address requesting the route. |
| `chainId` | body | `number` | no | Blockchain chain ID. Defaults to Ethereum mainnet when Torque provides a default. |
| `tokenIn` | body | `string` | yes | Input token address or addresses. |
| `tokenOut` | body | `string` | yes | Output token address or addresses. |
| `amountIn` | body | `string` | yes | Input amount or amounts in wei. |
| `slippage` | body | `string` | no | Slippage in basis points. Torque defaults to 50. |
| `routingStrategy` | body | `list` | no | Routing strategy. Torque defaults to delegate. Accepted values: `0`, `1`. |
