# Update Customer with GrooveHQ

Updates an existing customer in GrooveHQ.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/:customerEmail`
- **Base URL:** `https://api.groovehq.com/v1`
- **Official documentation:** [Update Customer](https://doc.groovehq.com/customers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerEmail` | path | `string` | yes |
| `email` | body | `string` | yes |
| `name` | body | `string` | no |
| `about` | body | `string` | no |
| `twitter_username` | body | `string` | no |
| `title` | body | `string` | no |
| `company_name` | body | `string` | no |
| `phone_number` | body | `string` | no |
| `location` | body | `string` | no |
| `linkedin_username` | body | `string` | no |
