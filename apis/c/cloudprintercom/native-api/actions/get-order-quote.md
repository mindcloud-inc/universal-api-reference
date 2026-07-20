# Get Order Quote with Cloudprinter.com

Retrieves an order quote from Cloudprinter.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/cloudcore/1.0/orders/quote`
- **Base URL:** `https://api.cloudprinter.com`
- **Official documentation:** [Get Order Quote](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#order-quote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | yes | Destination country in ISO 3166-1 alpha-2 format. |
| `state` | body | `string` | no | Destination state or region code when required for the selected country. |
| `currency` | body | `string` | no | Optional quote currency in ISO 4217 format. |
| `items[]` | body | `array<object>` | yes | One or more items to quote. |
| `items[].reference` | body | `string` | yes | Client-side reference for this quote item. |
| `items[].product` | body | `string` | yes | Cloudprinter product reference. |
| `items[].count` | body | `string` | yes | Quantity for this quote item. |
| `items[].options[]` | body | `array<object>` | no | Optional item options. Cloudprinter currently expects an array value even when empty. |
| `items[].options[].type` | body | `string` | yes | Option type from product info. |
| `items[].options[].count` | body | `string` | yes | Quantity for the selected option. |
