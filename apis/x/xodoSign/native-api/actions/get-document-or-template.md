# Get Document or Template with Xodo Sign

Retrieves a document or template from Xodo Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Get Document or Template](https://eversign.com/api/documentation/methods#get-document-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the document or template. |
| `document_hash` | query | `string` | yes | The unique document or template hash to retrieve. |
