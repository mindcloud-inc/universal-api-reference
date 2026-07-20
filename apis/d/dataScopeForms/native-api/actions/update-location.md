# Update Location with DataScope Forms

Updates an existing location in DataScope Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/external/locations/[:id]`
- **Base URL:** `https://www.mydatascope.com/api`
- **Official documentation:** [Update Location](https://dscope.github.io/docs/#update-a-location)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Internal identifier of the location to update. |
| `location.address` | body | `string` | no | Address of the location. |
| `location.city` | body | `string` | no | City of the location. |
| `location.code` | body | `string` | no | Code of the location. |
| `location.company_code` | body | `string` | no | Code of the company for the location. |
| `location.company_name` | body | `string` | no | Company name for the location. |
| `location.country` | body | `string` | no | Country of the location. |
| `location.description` | body | `string` | no | Description of the location. |
| `location.email` | body | `string` | no | Email of the location. |
| `location.latitude` | body | `number` | no | Latitude of the location. |
| `location.longitude` | body | `number` | no | Longitude of the location. |
| `location.name` | body | `string` | no | Name of the location. |
| `location.phone` | body | `string` | no | Phone number of the location. |
