# Delete Document or Template with Xodo Sign

Deletes an existing document or template from Xodo Sign.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Delete Document or Template](https://eversign.com/api/documentation/methods#delete-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the document or template. |
| `document_hash` | query | `string` | yes | The unique document or template hash to delete. |
