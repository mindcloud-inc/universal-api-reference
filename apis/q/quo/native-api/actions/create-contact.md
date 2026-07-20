# Create Contact with Quo

Creates a new contact in Quo.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.openphone.com/v1`
- **Official documentation:** [Create Contact](https://www.quo.com/docs/mdx/api-reference/contacts/create-a-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `createdByUserId` | body | `string` | no |
| `customFields[]` | body | `array<object>` | no |
| `defaultFields` | body | `object` | no |
| `defaultFields.company` | body | `string` | no |
| `defaultFields.emails[]` | body | `array<string>` | no |
| `defaultFields.firstName` | body | `string` | no |
| `defaultFields.lastName` | body | `string` | no |
| `defaultFields.phoneNumbers[]` | body | `array<string>` | no |
| `defaultFields.role` | body | `string` | no |
| `externalId` | body | `string` | no |
| `source` | body | `string` | no |
| `sourceUrl` | body | `string` | no |
