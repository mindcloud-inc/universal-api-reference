# Update Warehouse with Dukaan

Updates an existing warehouse in Dukaan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `api/store/seller/store-warehouse/v2/:warehouseUuid/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Update Warehouse](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `warehouseUuid` | path | `string` | yes | Warehouse UUID from Dukaan warehouse data. |
| `name` | body | `string` | no | Warehouse name. |
| `contact_person_name` | body | `string` | no | Warehouse contact person name. |
| `mobile_number` | body | `string` | no | Warehouse mobile number. |
| `pincode` | body | `string` | no | Warehouse postal code. |
| `address_line_1` | body | `string` | no | Warehouse address line 1. |
| `city` | body | `string` | no | Warehouse city. |
| `state` | body | `string` | no | Warehouse state. |
| `country` | body | `string` | no | Warehouse country code. |
| `store` | body | `number` | no | Store ID for the warehouse. |
