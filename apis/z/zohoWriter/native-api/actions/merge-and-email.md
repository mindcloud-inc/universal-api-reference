# Merge And Email with Zoho Writer

Merges a document and emails it in Zoho Writer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents/:document_id/merge/email`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [Merge And Email](https://www.zoho.com/writer/help/api/v1/inline-mail-merge-api.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The unique ID of the Zoho Writer document. |
| `subject` | body | `string` | yes | Email subject for the merge email. |
| `recipient_email` | body | `string` | yes | Recipient email address for the inline merge email. |
| `merge_data` | body | `string` | no | JSON string for merge_data, for example {"data":[{...}]}. |
