# Update Contact with Productlane

Updates an existing contact in Productlane.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:id`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Update Contact](https://productlane.mintlify.dev/docs/api/contacts/update-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `email` | body | `string` | no |
| `companyId` | body | `string` | no |
| `companyName` | body | `string` | no |
| `companyExternalId` | body | `string` | no |
