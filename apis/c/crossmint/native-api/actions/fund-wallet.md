# Fund Wallet with Crossmint

Funds a wallet in Crossmint.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1-alpha2/wallets/:walletLocator/balances`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Fund Wallet](https://docs.crossmint.com/api-reference/wallets/fund-wallet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator such as a wallet address or email:user@example.com:evm-smart-wallet. |
| `amount` | body | `number` | yes | Amount to fund, between 1 and 100. |
| `token` | body | `string` | yes | Funding token. Only usdxm is supported in staging. |
| `chain` | body | `string` | yes | Chain to fund on. Example: base-sepolia. |
