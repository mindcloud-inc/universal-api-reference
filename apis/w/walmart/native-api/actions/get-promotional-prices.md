# Get Promotional Prices with Walmart

Retrieves a list of promotional prices for a single SKU.

## Endpoint

- **Method:** `GET`
- **Path:** `v3/promo/sku/:sku`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Promotional Prices](https://developer.walmart.com/global-marketplace/reference/getpromotionalprices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sku` | path | `string` | yes | An arbitrary alphanumeric unique ID, specified by the seller, which identifies each item. This will be used by the seller in the XSD file to refer to each item. |
