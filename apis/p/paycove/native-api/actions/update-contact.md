# Update Contact with Paycove

Updates a contact in Paycove.

## Endpoint

- **Method:** `PATCH`
- **Path:** `contacts/:id`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Update Contact](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Paycove CRMContact ID. |
| `title` | query | `string` | no | Contact title. |
| `name` | query | `string` | no | Full contact name. |
| `first_name` | query | `string` | no | Contact first name. |
| `last_name` | query | `string` | no | Contact last name. |
| `email` | query | `string` | no | Contact email. |
| `phone` | query | `string` | no | Contact phone. |
| `mobile` | query | `string` | no | Contact mobile. |
| `line1` | query | `string` | no | Street address. |
| `city` | query | `string` | no | City. |
| `state` | query | `string` | no | State or region. |
| `country` | query | `string` | no | Country. |
| `postal_code` | query | `string` | no | Postal code. |
| `owner_id` | query | `string` | no | Contact owner ID. |
| `facebook` | query | `string` | no | Contact Facebook. |
| `twitter` | query | `string` | no | Contact Twitter. |
| `linkedin` | query | `string` | no | Contact LinkedIn. |
| `industry` | query | `string` | no | Contact industry. |
| `website` | query | `string` | no | Contact website. |
