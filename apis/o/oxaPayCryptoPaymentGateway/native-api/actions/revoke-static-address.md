# Revoke Static Address with OxaPay Crypto Payment Gateway

Deletes an existing static address from OxaPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/static-address/revoke`
- **Base URL:** `https://api.oxapay.com/v1`
- **Official documentation:** [Revoke Static Address](https://docs.oxapay.com/api-reference/payment/revoking-static-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Static address to revoke. |
| `network` | body | `string` | no | Blockchain network of the static address. |
