# Create Payment Link with Pinch Payments

Creates a payment link in Pinch Payments.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment-links`
- **Base URL:** `https://api.getpinch.com.au/live`
- **Official documentation:** [Create Payment Link](https://docs.getpinch.com.au/reference/create-payment-link)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `allowedPaymentMethods[]` | body | `array<string>` | yes |
| `amount` | body | `number` | yes |
| `currency` | body | `string` | no |
| `description` | body | `string` | yes |
| `linkExpiryDate` | body | `date` | no |
| `metadata` | body | `string` | no |
| `payerId` | body | `string` | yes |
| `returnUrl` | body | `string` | yes |
| `surchargePaymentMethods[]` | body | `array<string>` | no |
