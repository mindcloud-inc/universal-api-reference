# Create Realtime Payment with Pinch Payments

Creates a realtime payment in Pinch Payments.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/realtime`
- **Base URL:** `https://api.getpinch.com.au/live`
- **Official documentation:** [Create Realtime Payment](https://docs.getpinch.com.au/reference/realtime-payment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount` | body | `number` | yes |
| `applicationFee` | body | `number` | no |
| `description` | body | `string` | no |
| `email` | body | `string` | no |
| `firstName` | body | `string` | no |
| `fullName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `metadata` | body | `string` | no |
| `mobileNumber` | body | `string` | no |
| `nonce[]` | body | `array` | no |
| `payerId` | body | `string` | no |
| `sourceId` | body | `string` | no |
| `surcharge[]` | body | `array` | no |
| `token` | body | `string` | no |
