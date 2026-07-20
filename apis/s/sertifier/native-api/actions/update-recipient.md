# Update Recipient with Sertifier

Updates an existing recipient in Sertifier.

## Endpoint

- **Method:** `PUT`
- **Path:** `/recipient`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [Update Recipient](https://sertifier.docs.apiary.io/reference/recipient/add-update-recipient)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recipients[].id` | body | `string` | yes |
| `recipients[].name` | body | `string` | no |
| `recipients[].email` | body | `string` | no |
| `updateExistingCredentials` | body | `boolean` | no |
