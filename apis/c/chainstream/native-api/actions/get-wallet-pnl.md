# Get Wallet PnL with Chainstream

Retrieves wallet PnL from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/wallet/:chain/:walletAddress/pnl`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Wallet PnL](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-pnl-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks. |
| `walletAddress` | path | `string` | yes | An address of a wallet. |
| `resolution` | query | `string` | no | PnL time resolution (1d, 7d, 30d, or all). |
