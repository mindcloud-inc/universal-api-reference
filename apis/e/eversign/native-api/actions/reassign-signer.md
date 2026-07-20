# Reassign Signer with Eversign

Reassigns a signer on a document in Eversign.

## Endpoint

- **Method:** `POST`
- **Path:** `/reassign`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Reassign Signer](https://eversign.com/api/documentation/methods)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `document_hash` | body | `string` | yes |
| `signer_id` | body | `string` | yes |
| `new_signer_name` | body | `string` | yes |
| `new_signer_email` | body | `string` | yes |
| `reason` | body | `string` | no |
