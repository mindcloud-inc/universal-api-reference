# Copy Document with Zoho Writer

Creates a copy of a document in Zoho Writer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents/:document_id/copy`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [Copy Document](https://www.zoho.com/writer/help/api/v1/copy-document.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The unique ID of the Zoho Writer document. |
