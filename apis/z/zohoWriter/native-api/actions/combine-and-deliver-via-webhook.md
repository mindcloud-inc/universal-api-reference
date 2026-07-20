# Combine And Deliver Via Webhook with Zoho Writer

Combines documents and delivers them via webhook in Zoho Writer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents/pdf/combine/webhook`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [Combine And Deliver Via Webhook](https://www.zoho.com/writer/help/api/v1/combine-and-deliver-via-webhook.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files` | body | `file` | no | PDF files to combine. Provide either files or urls; Zoho requires at least 2 PDFs and allows up to 20. Send multiple values as a array. |
| `files1` | body | `file` | no | Second PDF file to combine. Use together with files for the required two-file minimum. |
| `urls` | body | `string` | no | Comma-separated public PDF URLs to combine. Provide either urls or files. |
| `webhook` | body | `string` | yes | JSON string describing the required webhook target, including invoke_url and any optional retry or header fields. |
| `output_settings` | body | `string` | no | JSON string for optional output_settings such as name and page_number_settings. |
