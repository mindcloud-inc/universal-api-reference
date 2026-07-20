# Create Quote with Prodigi

Retrieves Prodigi quotes for product and shipping costs.

## Endpoint

- **Method:** `POST`
- **Path:** `/quotes`
- **Base URL:** `https://api.prodigi.com/v4.0`
- **Official documentation:** [Create Quote](https://www.prodigi.com/print-api/docs/reference/#create-quote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destinationCountryCode` | body | `string` | yes | Two-letter ISO country code of the destination country. |
| `items[]` | body | `array<object>` | yes | Items to quote, including SKU, copies, attributes, and assets. |
| `shippingMethod` | body | `string` | no | Requested shipping method: budget, standard, standardplus, express, or overnight. |
| `currencyCode` | body | `string` | no | Three-letter ISO currency code. Defaults to the merchant settings when omitted. |
