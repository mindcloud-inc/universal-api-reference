# Merge Document with Zoho Writer

Merges a document in Zoho Writer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents/:document_id/merge`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [Merge Document](https://www.zoho.com/writer/help/api/v1/merge-document.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The unique ID of the Zoho Writer document. |
| `output_settings` | body | `string` | yes | JSON string for the required output_settings payload. At minimum pass the format to generate, for example {"format":"pdf"}. |
| `merge_data` | body | `string` | no | JSON string for merge_data, for example {"data":[{...}]}. |
| `record_id` | body | `string` | no | Alternative to merge_data for supported Zoho CRM, Creator, and Bigin templates. |
