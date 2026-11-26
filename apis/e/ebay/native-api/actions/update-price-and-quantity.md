# Update - Price and Quantity with eBay

## Endpoint

- **Method:** `POST`
- **Path:** `sell/inventory/v1/bulk_update_price_quantity`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Update - Price and Quantity](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/updateOffer)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `requests[].shipToLocationAvailability` | body | `object` | no |
| `requests[].shipToLocationAvailability.quantity` | body | `number` | no |
| `requests[].sku` | body | `string` | no |
| `requests[]` | body | `array` | no |
