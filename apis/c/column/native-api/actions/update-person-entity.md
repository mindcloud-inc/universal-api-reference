# Update Person Entity with Column

## Endpoint

- **Method:** `PATCH`
- **Path:** `/entities/person/:entity_id`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Update Person Entity](https://column.com/docs/api/#entity/update-person)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity_id` | path | `string` | yes |
| `first_name` | body | `string` | yes |
| `middle_name` | body | `string` | no |
| `last_name` | body | `string` | yes |
| `ssn` | body | `string` | yes |
| `date_of_birth` | body | `string` | yes |
| `address.line_1` | body | `string` | yes |
| `address.city` | body | `string` | yes |
| `address.state` | body | `string` | yes |
| `address.postal_code` | body | `string` | yes |
| `address.country_code` | body | `string` | yes |
