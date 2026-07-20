# Create Location with More Good Reviews

Creates a location in More Good Reviews.

## Endpoint

- **Method:** `POST`
- **Path:** `/beacon/locations`
- **Base URL:** `https://api.moregoodreviews.com`
- **Official documentation:** [Create Location](https://docs.moregoodreviews.com/platform/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the location. |
| `display_name` | body | `string` | no | The customer-facing name for the location. Falls back to name. |
| `slug` | body | `string` | no | The slug for the location. Generated if left out. |
| `code` | body | `string` | no | An optional store code. |
| `address1` | body | `string` | no | Address line 1. |
| `address2` | body | `string` | no | Address line 2. |
| `city` | body | `string` | no | The city or town. |
| `state` | body | `string` | no | The state or region. |
| `postal_code` | body | `string` | no | The postal code. |
