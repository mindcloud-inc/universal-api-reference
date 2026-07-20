# Get Enso Approval Transaction with Torque

## Endpoint

- **Method:** `POST`
- **Path:** `/enso/approval`
- **Base URL:** `https://app.torque.fi/api`
- **Official documentation:** [Get Enso Approval Transaction](https://docs.torque.fi/business/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromAddress` | body | `string` | yes | Wallet address that would approve token spending. |
| `tokenAddress` | body | `string` | yes | Token contract address. |
| `chainId` | body | `number` | no | Blockchain chain ID. Defaults to Ethereum mainnet when Torque provides a default. |
| `amount` | body | `string` | yes | Amount in wei. |
| `routingStrategy` | body | `list` | no | Routing strategy. Torque defaults to router. Accepted values: `0`, `1`. |
