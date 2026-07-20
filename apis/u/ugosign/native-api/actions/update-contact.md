# Update Contact with Ugosign

Updates an existing contact in Ugosign.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/contacts/:contact`
- **Base URL:** `https://app.ugosign.com/api`
- **Official documentation:** [Update Contact](https://app.ugosign.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `city` | body | `string` | no |
| `contact` | path | `string` | yes |
| `country` | body | `string` | no |
| `email` | body | `string` | yes |
| `family_name` | body | `string` | no |
| `given_name` | body | `string` | no |
| `phone_number` | body | `string` | no |
| `website` | body | `string` | no |
