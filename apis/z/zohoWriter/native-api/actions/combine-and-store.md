# Combine And Store with Zoho Writer

Combines documents and stores them in Zoho Writer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents/pdf/combine/store`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [Combine And Store](https://www.zoho.com/writer/help/api/v1/combine-and-store.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files` | body | `file` | no | PDF files to combine. Provide either files or urls; Zoho requires at least 2 PDFs and allows up to 20. Send multiple values as a array. |
| `files` | body | `file` | no | Second PDF file to combine. Use together with files for the required two-file minimum. |
| `urls` | body | `string` | no | Comma-separated public PDF URLs to combine. Provide either urls or files. |
| `output_settings` | body | `string` | no | JSON string for optional output_settings such as name, folder_id, and overwrite_existing_file. |
