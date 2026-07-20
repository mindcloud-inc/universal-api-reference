# Create Wallet Top-Up with Strale

Creates a wallet top-up checkout session in Strale.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/wallet/topup`
- **Base URL:** `https://api.strale.io`
- **Official documentation:** [Create Wallet Top-Up](https://api.strale.io/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount_cents` | body | `number` | yes | Top-up amount in euro cents. |
