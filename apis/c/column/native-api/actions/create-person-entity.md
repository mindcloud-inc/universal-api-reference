# Create Person Entity with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/entities/person`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Create Person Entity](https://column.com/docs/api/#entity/create-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | First name of the individual. |
| `last_name` | body | `string` | yes | Last name of the individual. |
| `ssn` | body | `string` | yes | Social Security Number. |
| `date_of_birth` | body | `string` | yes | Date of birth in YYYY-MM-DD format. |
| `address.line_1` | body | `string` | yes | Street address line 1. |
| `address.city` | body | `string` | yes | City. |
| `address.state` | body | `string` | yes | State or province. |
| `address.postal_code` | body | `string` | yes | Postal code. |
| `address.country_code` | body | `string` | yes | ISO 3166-1 Alpha-2 country code. |
