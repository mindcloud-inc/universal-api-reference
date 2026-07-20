# Create or Update Supplier with Loyverse

Creates or updates a supplier in Loyverse.

## Endpoint

- **Method:** `POST`
- **Path:** `/suppliers/`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [Create or Update Supplier](https://developer.loyverse.com/docs/#tag/Suppliers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | The supplier id. If included in the POST request it will cause an update instead of a creating a new object. |
| `name` | body | `string` | yes | The supplier company name |
| `contact` | body | `string` | no | The supplier contact person name |
| `email` | body | `string` | no | The supplier email |
| `phone_number` | body | `string` | no | — |
| `website` | body | `string` | no | The supplier website page |
| `address_1` | body | `string` | no | The supplier address |
| `address_2` | body | `string` | no | The supplier address |
| `city` | body | `string` | no | The supplier city, town, or village. |
| `region` | body | `string` | no | The supplier’s region name. Typically a province, a state, or a prefecture. |
| `postal_code` | body | `string` | no | The supplier’s postal code, also known as zip, postcode, Eircode, etc. |
| `country_code` | body | `string` | no | The two-letter country code corresponding to the supplier country in ISO 3166-1-alpha-2 format. |
| `note` | body | `string` | no | — |
| `created_at` | body | `date` | no | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `updated_at` | body | `date` | no | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `deleted_at` | body | `date` | no | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
