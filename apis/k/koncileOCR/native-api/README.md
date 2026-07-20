# Koncile OCR: Native API Reference

A consolidated summary of Koncile OCR's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.koncile.ai/api-setup/getting-started
- **OpenAPI specification:** https://api.koncile.ai
- **API base URL:** `https://api.koncile.ai/v1`

## Authentication

### API Key

Use a Koncile API key generated in Settings > API. The Koncile REST API expects Authorization: Bearer <API_KEY>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.koncile.ai/api-setup/getting-started)

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check API Key](actions/check-api-key.md) | `POST /check_api_key` | [docs](https://docs.koncile.ai/api-setup/getting-started) |
| [Create Field](actions/create-field.md) | `POST /create_field` | [docs](https://docs.koncile.ai/api-setup/fields) |
| [Create Folder](actions/create-folder.md) | `POST /create_folder` | [docs](https://docs.koncile.ai/api-setup/folders) |
| [Create Instruction](actions/create-instruction.md) | `POST /create_instruction` | [docs](https://docs.koncile.ai/api-setup/instructions) |
| [Create Template](actions/create-template.md) | `POST /create_template` | [docs](https://docs.koncile.ai/api-setup/templates) |
| [Delete Document](actions/delete-document.md) | `DELETE /delete_doc` | [docs](https://docs.koncile.ai/api-setup/documents) |
| [Delete Field](actions/delete-field.md) | `DELETE /delete_field` | [docs](https://docs.koncile.ai/api-setup/fields) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /delete_folder` | [docs](https://docs.koncile.ai/api-setup/folders) |
| [Delete Instruction](actions/delete-instruction.md) | `DELETE /delete_instruction` | [docs](https://docs.koncile.ai/api-setup/instructions) |
| [Delete Template](actions/delete-template.md) | `DELETE /delete_template` | [docs](https://docs.koncile.ai/api-setup/templates) |
| [Download File](actions/download-file.md) | `GET /fetch_file` | [docs](https://docs.koncile.ai/api-setup/documents) |
| [Download Files Batch](actions/download-files-batch.md) | `POST /fetch_files_batch` | [docs](https://docs.koncile.ai/api-setup/documents) |
| [Get Document Data](actions/get-document-data.md) | `GET /fetch_document_data` | [docs](https://docs.koncile.ai/api-setup/documents) |
| [Get Field](actions/get-field.md) | `GET /fetch_field` | [docs](https://docs.koncile.ai/api-setup/fields) |
| [Get Folder](actions/get-folder.md) | `GET /fetch_folder` | [docs](https://docs.koncile.ai/api-setup/folders) |
| [Get Instruction](actions/get-instruction.md) | `GET /fetch_instruction` | [docs](https://docs.koncile.ai/api-setup/instructions) |
| [Get Template](actions/get-template.md) | `GET /fetch_template` | [docs](https://docs.koncile.ai/api-setup/templates) |
| [List Documents](actions/list-documents.md) | `GET /fetch_documents` | [docs](https://docs.koncile.ai/api-setup/documents) |
| [List Folders](actions/list-folders.md) | `GET /fetch_all_folders` | [docs](https://docs.koncile.ai/api-setup/folders) |
| [Retrieve Task Result](actions/retrieve-task-result.md) | `GET /fetch_tasks_results` | [docs](https://docs.koncile.ai/api-setup/task-retrieval) |
| [Update Field](actions/update-field.md) | `PUT /update_field` | [docs](https://docs.koncile.ai/api-setup/fields) |
| [Update Folder](actions/update-folder.md) | `PUT /update_folder` | [docs](https://docs.koncile.ai/api-setup/folders) |
| [Update Instruction](actions/update-instruction.md) | `PUT /update_instruction` | [docs](https://docs.koncile.ai/api-setup/instructions) |
| [Update Template](actions/update-template.md) | `PUT /update_template` | [docs](https://docs.koncile.ai/api-setup/templates) |
| [Upload File](actions/upload-file.md) | `POST /upload_file` | [docs](https://docs.koncile.ai/api-setup/file-uploading) |
