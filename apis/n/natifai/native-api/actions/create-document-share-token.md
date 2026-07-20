# Create Document Share Token with Natif.ai

Creates a document sharing token in Natif.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/share-tokens/documents`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Create Document Share Token](https://api.natif.ai/docs#/Document%20Capturing/create_share_token_share_tokens_documents_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | body | `string` | yes | UUID of the document to share. |
| `expires_at` | body | `string` | yes | Expiration date for the share token in YYYY-MM-DD format. Tokens expire at 00:00:00 UTC on this date. |
