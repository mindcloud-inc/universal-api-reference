# Create Property with Wasi

Creates a new property in Wasi.

## Endpoint

- **Method:** `POST`
- **Path:** `/property/add`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [Create Property](https://api.wasi.co/docs/en/guide/properties.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | no | Property address. |
| `area` | query | `number` | no | Property area. |
| `bathrooms` | query | `number` | no | Bathroom count. |
| `bedrooms` | query | `number` | no | Bedroom count. |
| `built_area` | query | `number` | no | Built area. |
| `for_rent` | query | `boolean` | no | Whether the property is for rent. |
| `for_sale` | query | `boolean` | no | Whether the property is for sale. |
| `for_transfer` | query | `boolean` | no | Whether the property is for transfer. |
| `garages` | query | `number` | no | Garage count. |
| `id_city` | query | `number` | no | City ID. |
| `id_country` | query | `number` | no | Country ID. |
| `id_location` | query | `number` | no | Locality ID. |
| `id_property_type` | query | `number` | no | Property type ID. |
| `id_region` | query | `number` | no | Region ID. |
| `observations` | query | `string` | no | Property observations. |
| `rent_price` | query | `number` | no | Property rent price. |
| `sale_price` | query | `number` | no | Property sale price. |
| `title` | query | `string` | no | Property title. |
