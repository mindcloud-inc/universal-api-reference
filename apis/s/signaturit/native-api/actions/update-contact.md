# Update Contact with Signaturit

Updates an existing contact in Signaturit.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:id.json`
- **Base URL:** `https://api.sandbox.signaturit.com/v3`
- **API:** rest
- **Official documentation:** [Update Contact](https://docs.signaturit.com/api/latest#contacts_patch_contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier of the contact to update. |
| `name` | body | `string` | no | Updated contact name. |
| `email` | body | `string` | no | Updated contact email. |
