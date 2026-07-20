# Update Contact with GetSales.io

## Endpoint

- **Method:** `PUT`
- **Path:** `/leads/api/leads/{uuid}`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [Update Contact](https://api.getsales.io/api/openapi/contacts/updatelead.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | UUID of the contact to update. |
| `first_name` | body | `string` | no | Contact first name. |
| `last_name` | body | `string` | no | Contact last name. |
| `company_name` | body | `string` | no | Contact company name. |
| `email` | body | `string` | no | Contact email address. |
| `linkedin` | body | `string` | no | LinkedIn profile handle. |
| `position` | body | `string` | no | Contact job title or position. |
