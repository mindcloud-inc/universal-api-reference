# Update Contact By ID with Quo

Updates an existing contact in Quo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.openphone.com/v1`
- **Official documentation:** [Update Contact By ID](https://www.quo.com/docs/mdx/api-reference/contacts/update-a-contact-by-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customFields[]` | body | `array<object>` | no |
| `defaultFields` | body | `object` | no |
| `defaultFields.company` | body | `string` | no |
| `defaultFields.emails[]` | body | `array<string>` | no |
| `defaultFields.firstName` | body | `string` | no |
| `defaultFields.lastName` | body | `string` | no |
| `defaultFields.phoneNumbers[]` | body | `array<string>` | no |
| `defaultFields.role` | body | `string` | no |
| `externalId` | body | `string` | no |
| `id` | path | `string` | yes |
| `source` | body | `string` | no |
| `sourceUrl` | body | `string` | no |
