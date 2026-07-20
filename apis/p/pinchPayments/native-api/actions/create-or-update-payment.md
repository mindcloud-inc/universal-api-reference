# Create or Update Payment with Pinch Payments

Creates or updates a scheduled payment in Pinch Payments.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments`
- **Base URL:** `https://api.getpinch.com.au/live`
- **Official documentation:** [Create or Update Payment](https://docs.getpinch.com.au/reference/save-payment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount` | body | `number` | yes |
| `applicationFee` | body | `number` | no |
| `description` | body | `string` | no |
| `id` | body | `string` | no |
| `nonce[]` | body | `array` | no |
| `payerId` | body | `string` | yes |
| `sourceId` | body | `string` | no |
| `surcharge[]` | body | `array` | no |
| `transactionDate` | body | `date` | yes |
