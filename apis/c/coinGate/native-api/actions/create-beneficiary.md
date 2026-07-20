# Create Beneficiary with CoinGate

Creates a new beneficiary in CoinGate.

## Endpoint

- **Method:** `POST`
- **Path:** `/beneficiaries`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [Create Beneficiary](https://developer.coingate.com/reference/create-beneficiary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `beneficiary_type` | body | `string` | yes | Beneficiary type. |
| `email` | body | `string` | yes | Beneficiary email. |
| `country` | body | `string` | yes | Beneficiary country. |
| `currency_id` | body | `number` | yes | CoinGate currency ID. |
| `platform_id` | body | `number` | yes | CoinGate platform ID. |
| `crypto_address` | body | `string` | yes | Beneficiary crypto address. |
