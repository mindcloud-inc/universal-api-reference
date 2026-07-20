# Create/Upload Documents with Zoho Writer

Creates or uploads a document in Zoho Writer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [Create/Upload Documents](https://www.zoho.com/writer/help/api/v1/create-upload-documents.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | no | Name for the new Writer document. |
| `resource_type` | body | `string` | no | Optional document type to create: fillable, merge, or sign. |
