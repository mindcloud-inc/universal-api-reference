# Create Template Draft with Eversign

Creates a draft template in Eversign.

## Endpoint

- **Method:** `POST`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Create Template Draft](https://eversign.com/api/documentation/methods)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `is_draft` | body | `string` | no |
| `is_template` | body | `string` | no |
| `reminders` | body | `string` | no |
| `require_all_signers` | body | `string` | no |
| `sandbox` | body | `string` | no |
| `signers[0].id` | body | `string` | no |
| `signers[0].required` | body | `string` | no |
| `use_signer_order` | body | `string` | no |
| `files[0].file_id` | body | `string` | yes |
| `signers[0].role` | body | `string` | yes |
