# Calculate Wallet PnL with Chainstream

Calculates wallet token PnL in Chainstream.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/wallet/:chain/:walletAddress/calculate-pnl`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Calculate Wallet PnL](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-calculate-pnl-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks. |
| `walletAddress` | path | `string` | yes | An address of a wallet. |
| `tokenAddresses[]` | body | `array<string>` | no | Token addresses to include in the calculation. |
