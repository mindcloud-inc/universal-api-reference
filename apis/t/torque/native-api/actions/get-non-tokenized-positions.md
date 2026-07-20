# Get Non Tokenized Positions with Torque

## Endpoint

- **Method:** `GET`
- **Path:** `/enso/positions/nontokenized`
- **Base URL:** `https://app.torque.fi/api`
- **Official documentation:** [Get Non Tokenized Positions](https://docs.torque.fi/business/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eoaAddress` | query | `string` | yes | Externally owned account wallet address. Torque's live endpoint currently requires eoaAddress for this route. |
| `chainId` | query | `number` | no | Blockchain chain ID. Defaults to Ethereum mainnet when Torque provides a default. |
