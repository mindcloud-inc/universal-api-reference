# Create Address with Lob

## Endpoint

- **Method:** `POST`
- **Path:** `/addresses`
- **Base URL:** `https://api.lob.com/v1`
- **Official documentation:** [Create Address](https://docs.lob.com/#tag/Addresses/operation/address_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The recipient name for the address. |
| `address_line1` | body | `string` | yes | The primary street address line. |
| `address_line2` | body | `string` | no | The secondary street address line. |
| `address_city` | body | `string` | yes | The city for the address. |
| `address_state` | body | `string` | yes | The state or region for the address. |
| `address_zip` | body | `string` | yes | The ZIP or postal code for the address. |
