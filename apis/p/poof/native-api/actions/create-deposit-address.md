# Create Deposit Address with Poof

Creates a new deposit address in Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `https://www.poof.io/api/v2/create_charge`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Create Deposit Address](https://docs.poof.io/reference/create_address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `string` | yes | Deposit address quote amount from the docs example. |
| `crypto` | body | `string` | yes | Crypto asset code from the docs example. |
| `metadata.example` | body | `string` | yes | Nested metadata value from the docs example. |
