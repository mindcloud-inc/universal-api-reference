# Create Contact with Productlane

Creates a new contact in Productlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Create Contact](https://productlane.mintlify.dev/docs/api/contacts/create-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `name` | body | `string` | no |
| `companyId` | body | `string` | no |
| `companyName` | body | `string` | no |
| `companyExternalId` | body | `string` | no |
