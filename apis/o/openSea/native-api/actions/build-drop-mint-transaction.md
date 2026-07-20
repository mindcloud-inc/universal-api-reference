# Build Mint Transaction Data For Drop with OpenSea

Builds mint transaction data for an OpenSea drop.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/drops/{slug}/mint`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Build Mint Transaction Data For Drop](https://docs.opensea.io/reference/build_drop_mint_transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | The collection slug identifying the drop |
| `minter` | body | `string` | yes | Wallet address that will receive the minted tokens |
| `quantity` | body | `number` | yes | Number of tokens to mint |
