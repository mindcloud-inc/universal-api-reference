# Get Photobook Spine Details with Prodigi

Retrieves the required spine width for a Prodigi photobook.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/spine`
- **Base URL:** `https://api.prodigi.com/v4.0`
- **Official documentation:** [Get Photobook Spine Details](https://www.prodigi.com/print-api/docs/reference/#get-photobook-spine-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sku` | body | `string` | yes | Photobook product SKU. |
| `destinationCountryCode` | body | `string` | yes | Two-letter ISO country code for the destination country. |
| `state` | body | `string` | no | Destination state, used when needed for the destination country. |
| `numberOfPages` | body | `number` | yes | Number of pages in the photobook. |
