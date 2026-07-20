# Create Contact with Omnisend

Creates a contact in Omnisend, or updates an existing one.

## Endpoint

- **Method:** `POST`
- **Path:** `/v5/contacts`
- **Base URL:** `https://api.omnisend.com`
- **Official documentation:** [Create Contact](https://api-docs.omnisend.com/reference/post_contacts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address` | body | `string` | no |
| `birthdate` | body | `date` | no |
| `city` | body | `string` | no |
| `country` | body | `string` | no |
| `countryCode` | body | `string` | no |
| `firstName` | body | `string` | no |
| `gender` | body | `string` | no |
| `identifiers[]` | body | `array<object>` | yes |
| `identifiers[].channels` | body | `object` | no |
| `identifiers[].channels.email` | body | `object` | no |
| `identifiers[].channels.email.status` | body | `string` | no |
| `identifiers[].channels.email.statusDate` | body | `date` | no |
| `identifiers[].id` | body | `string` | yes |
| `identifiers[].sendWelcomeMessage` | body | `boolean` | no |
| `identifiers[].type` | body | `string` | yes |
| `lastName` | body | `string` | no |
| `postalCode` | body | `string` | no |
