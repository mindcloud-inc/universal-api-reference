# Create Product with HubSpot

Creates a new product in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/products`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Product](https://developers.hubspot.com/docs/api-reference/crm-products-v3/basic/post-crm-v3-objects-products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties` | body | `object` | yes | Product property values object. |
| `associations[]` | body | `array<object>` | no | Optional associations for the new product. |
