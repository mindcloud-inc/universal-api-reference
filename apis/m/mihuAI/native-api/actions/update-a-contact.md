# Update a Contact with Mihu AI

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/contacts/:uuid`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Update a Contact](https://developers.mihu.ai/api-reference/contacts/update-a-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `country_code` | body | `string` | no |
| `email` | body | `string` | no |
| `name` | body | `string` | no |
| `phone_number` | body | `string` | no |
| `primary_language` | body | `string` | no |
| `status` | body | `string` | no |
| `surname` | body | `string` | no |
| `timezone` | body | `string` | no |
| `uuid` | path | `string` | yes |
