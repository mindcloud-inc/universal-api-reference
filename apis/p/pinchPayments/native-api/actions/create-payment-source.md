# Create Payment Source with Pinch Payments

Creates a payment source in Pinch Payments.

## Endpoint

- **Method:** `POST`
- **Path:** `/payers/[:id]/sources`
- **Base URL:** `https://api.getpinch.com.au/live`
- **Official documentation:** [Create Payment Source](https://docs.getpinch.com.au/reference/create-payment-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bankAccountBsb` | body | `string` | no | The BSB for the payer's bank account. |
| `bankAccountName` | body | `string` | no | The name for the payer's bank account. |
| `bankAccountNumber` | body | `string` | no | The bank account number for the payer's bank account. |
| `id` | path | `string` | yes | Payer ID in pyr_XXXXXXXXXXXXXX format. |
| `ipAddress` | body | `string` | no | The IP address associated with the payment source. |
| `sourceType` | body | `string` | no | Currently either bank-account or credit-card. |
| `token` | body | `string` | no | The token created by the capture script for the payment source. |
