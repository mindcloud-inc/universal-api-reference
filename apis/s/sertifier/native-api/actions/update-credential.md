# Update Credential with Sertifier

Updates an existing credential in Sertifier.

## Endpoint

- **Method:** `PUT`
- **Path:** `/credential/:credential_id`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [Update Credential](https://sertifier.docs.apiary.io/reference/credential/get-update-delete-credential)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `credential_id` | path | `string` | yes |
| `name` | body | `string` | no |
| `issueDate` | body | `date` | no |
| `expireDate` | body | `date` | no |
