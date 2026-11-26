# Bulk Migrate Listings with eBay

Create a new Inventory Location.

## Endpoint

- **Method:** `POST`
- **Path:** `sell/inventory/v1/bulk_migrate_listing`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Bulk Migrate Listings](https://developer.ebay.com/api-docs/sell/inventory/resources/location/methods/createInventoryLocation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `requests[]` | body | `array` | no |
| `requests[].listingId` | body | `string` | no |
