# Reassign Signer with Xodo Sign

Reassigns a document signer to another person in Xodo Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/reassign`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Reassign Signer](https://eversign.com/api/documentation/methods#reassign-signer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | Business ID to scope the reassignment request. |
| `document_hash` | body | `string` | yes | Unique document hash whose signer should be reassigned. |
| `signer_id` | body | `string` | yes | Signer ID that should be replaced. |
| `new_signer_name` | body | `string` | yes | Display name of the replacement signer. |
| `new_signer_email` | body | `string` | yes | Email address of the replacement signer. |
| `reason` | body | `string` | no | Optional reason for the reassignment. |
