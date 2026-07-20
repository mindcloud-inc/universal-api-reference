# Rename Document with Zoho Writer

Renames a document in Zoho Writer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents/:document_id/meta`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [Rename Document](https://www.zoho.com/writer/help/api/v1/rename-document.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The unique ID of the Zoho Writer document. |
| `operations` | body | `object` | yes | — |
