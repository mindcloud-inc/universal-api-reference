# Update Property with Channex

Updates an existing property in Channex.

## Endpoint

- **Method:** `PUT`
- **Path:** `/properties/:id`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Update Property](https://docs.channex.io/api-v.1-documentation/hotels-collection#update-property)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the property to update. |
| `property` | body | `object` | yes | Top-level property payload object documented by Channex for property updates. |
