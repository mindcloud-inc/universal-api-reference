# Get Shipping Options with Lulu

Retrieves shipping options from Lulu.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipping-options/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Get Shipping Options](https://api.lulu.com/docs/#tag/Shipping-Options/operation/retrieve-shipping-options)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `line_items[]` | body | `array` | yes | Array of Lulu line items to price for shipping. |
| `shipping_address` | body | `object` | yes | Shipping address for the available shipping options lookup. |
