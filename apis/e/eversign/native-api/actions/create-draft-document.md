# Create Draft Document with Eversign

Creates a draft document in Eversign.

## Endpoint

- **Method:** `POST`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Create Draft Document](https://eversign.com/api/documentation/methods)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `embedded_signing_enabled` | body | `string` | no |
| `flexible_signing` | body | `string` | no |
| `is_draft` | body | `string` | no |
| `reminders` | body | `string` | no |
| `require_all_signers` | body | `string` | no |
| `sandbox` | body | `string` | no |
| `signers[0].id` | body | `string` | no |
| `use_hidden_tags` | body | `string` | no |
| `use_signer_order` | body | `string` | no |
| `files[0].file_id` | body | `string` | yes |
| `signers[0].name` | body | `string` | yes |
| `signers[0].email` | body | `string` | yes |
