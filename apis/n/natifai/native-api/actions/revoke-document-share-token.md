# Revoke Document Share Token with Natif.ai

Deletes an existing document sharing token from Natif.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/share-tokens/documents`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Revoke Document Share Token](https://api.natif.ai/docs#/Document%20Capturing/revoke_doc_sharing_tokens_share_tokens_documents_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token_uuid` | query | `string` | yes | UUID of the sharing token to revoke. |
