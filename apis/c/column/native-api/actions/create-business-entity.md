# Create Business Entity with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/entities/business`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Create Business Entity](https://column.com/docs/api/#entity/create-business)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_name` | body | `string` | yes | Legal business name. |
| `ein` | body | `string` | yes | Employer Identification Number. |
| `legal_type` | body | `list` | no | Type of business. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `address.line_1` | body | `string` | yes | Street address line 1. |
| `address.city` | body | `string` | yes | City. |
| `address.state` | body | `string` | yes | State or province. |
| `address.postal_code` | body | `string` | yes | Postal code. |
| `address.country_code` | body | `string` | yes | ISO 3166-1 Alpha-2 country code. |
| `is_root` | body | `boolean` | no | Whether the business is a root entity. |
