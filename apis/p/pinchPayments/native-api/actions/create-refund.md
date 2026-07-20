# Create Refund with Pinch Payments

Creates a refund in Pinch Payments.

## Endpoint

- **Method:** `POST`
- **Path:** `/refunds`
- **Base URL:** `https://api.getpinch.com.au/live`
- **Official documentation:** [Create Refund](https://docs.getpinch.com.au/reference/create-a-refund)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount` | body | `number` | yes |
| `nonce` | body | `string` | no |
| `paymentId` | body | `string` | yes |
| `reason` | body | `string` | yes |
