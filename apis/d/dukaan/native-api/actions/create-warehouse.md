# Create Warehouse with Dukaan

Creates a new warehouse in Dukaan.

## Endpoint

- **Method:** `POST`
- **Path:** `api/store/seller/store-warehouse/v2/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Create Warehouse](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Warehouse name. |
| `contact_person_name` | body | `string` | yes | Warehouse contact person name. |
| `mobile_number` | body | `string` | yes | Warehouse mobile number. |
| `pincode` | body | `string` | yes | Warehouse postal code. |
| `address_line_1` | body | `string` | yes | Warehouse address line 1. |
| `city` | body | `string` | yes | Warehouse city. |
| `state` | body | `string` | yes | Warehouse state. |
| `country` | body | `string` | yes | Warehouse country code. |
| `terms_checked` | body | `boolean` | no | Whether terms were checked. |
