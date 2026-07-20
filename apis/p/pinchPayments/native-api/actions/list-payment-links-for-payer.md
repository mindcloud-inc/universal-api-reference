# List Payment Links for Payer with Pinch Payments

Retrieves payment links for a payer from Pinch Payments.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment-links/payer/[:payerId]`
- **Base URL:** `https://api.getpinch.com.au/live`
- **Official documentation:** [List Payment Links for Payer](https://docs.getpinch.com.au/reference/get-payment-links-by-payer)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `payerId` | path | `string` | yes |
