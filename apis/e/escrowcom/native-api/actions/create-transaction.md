# Create Transaction with Escrow.com

Creates a new transaction in Escrow.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/transaction`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Create Transaction](https://www.escrow.com/api/docs/create-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency` | body | `string` | yes | Transaction currency, such as usd. |
| `description` | body | `string` | yes | Transaction description. |
| `items[]` | body | `array<object>` | yes | Transaction items array. |
| `parties[]` | body | `array<object>` | yes | Transaction parties array. |
| `reference` | body | `string` | no | Optional external reference for lookup through Get Transaction by Reference. |
