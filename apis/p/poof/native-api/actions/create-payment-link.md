# Create Payment Link with Poof

Creates a new payment link in Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `/create_invoice`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Create Payment Link](https://docs.poof.io/reference/createinvoice-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `string` | yes | Payment link amount. |
| `crypto` | body | `string` | yes | Crypto asset code. |
| `metadata.example` | body | `string` | yes | Nested metadata value from the docs example. |
