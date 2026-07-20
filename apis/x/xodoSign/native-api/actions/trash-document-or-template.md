# Trash Document or Template with Xodo Sign

Moves a document or template to trash in Xodo Sign.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Trash Document or Template](https://eversign.com/api/documentation/methods#trash-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the document or template. |
| `document_hash` | query | `string` | yes | The unique document or template hash to trash. |
