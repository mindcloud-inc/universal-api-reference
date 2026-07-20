# Retrieve Voucher Payments with Lexware Office

Retrieves payment information for a voucher in Lexware Office.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/payments/:voucherId`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Retrieve Voucher Payments](https://developers.lexware.io/docs/#payments-endpoint-retrieve-payment-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voucherId` | path | `string` | yes | Voucher ID from Lexware. |
