# Create Payment Link with Fintoc

Creates a payment link in Fintoc.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/payment_links`
- **Base URL:** `https://api.fintoc.com`
- **Official documentation:** [Create Payment Link](https://docs.fintoc.com/reference/create-payment-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Amount in minor units for the payment link. |
| `currency` | body | `string` | yes | ISO currency code. This test account accepts MXN. |
