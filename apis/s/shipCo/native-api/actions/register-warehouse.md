# Register Warehouse with Ship&Co

## Endpoint

- **Method:** `POST`
- **Path:** `/warehouses`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [Register Warehouse](https://developer.shipandco.com/en/#warehouse)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | Warehouse company name. |
| `email` | body | `string` | no | Warehouse email address. |
| `full_name` | body | `string` | no | Warehouse contact full name. Required unless another supported name field is present. |
| `province_kanji` | body | `string` | no | Required for warehouses located in Japan. |
| `country` | body | `string` | yes | ISO country code. |
| `zip` | body | `string` | yes | Postal code. |
| `address1` | body | `string` | yes | Primary warehouse address. |
| `phone` | body | `string` | yes | Warehouse phone number. |
