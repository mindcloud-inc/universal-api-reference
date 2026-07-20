# Update Register Products with KEYZY

Registers a KEYZY product to a licensee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/register-products/:serial`
- **Base URL:** `https://api.keyzy.io/v2`
- **Official documentation:** [Update Register Products](https://www.keyzy.io/docs/developers/rest-api/licenses-register-products-edit/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email of the user. |
| `name` | body | `string` | yes | Name of the user. |
| `serial` | path | `string` | yes | A license serial number. |
| `sku_number` | body | `string` | yes | SKU number. |
