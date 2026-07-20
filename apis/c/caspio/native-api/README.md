# Caspio: Native API Reference

A consolidated summary of Caspio's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://d2hbw900.caspio.com/integrations/rest/swagger
- **OpenAPI specification:** https://d2hbw900.caspio.com/integrations/rest/v3/swagger/documentation
- **API base URL:** `https://d2hbw900.caspio.com/integrations/rest`

## Authentication

### OAuth 2.0

OAuth 2.0 client-credentials flow for the d2hbw900 Caspio tenant.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://d2hbw900.caspio.com/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://howto.caspio.com/integrate-your-apps/web-services-api/authenticating-rest/)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Table Record](actions/create-table-record.md) | `POST /v3/tables/{tableName}/records` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/CreateTableRecord) |
| [Create View Record](actions/create-view-record.md) | `POST /v3/views/{viewName}/records` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/CreateViewRecord) |
| [Delete Table Attachment](actions/delete-table-attachment.md) | `DELETE /v3/tables/{tableName}/attachments/{attachmentFieldName}` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/DeleteFileFromAttachmentTableFields) |
| [Delete Table Records](actions/delete-table-records.md) | `DELETE /v3/tables/{tableName}/records` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/DeleteTableRecords) |
| [Delete View Attachment](actions/delete-view-attachment.md) | `DELETE /v3/views/{viewName}/attachments/{attachmentFieldName}` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/DeleteFileFromAttachmentViewFields) |
| [Delete View Records](actions/delete-view-records.md) | `DELETE /v3/views/{viewName}/records` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/DeleteViewRecords) |
| [Download Table Attachment](actions/download-table-attachment.md) | `GET /v3/tables/{tableName}/attachments/{attachmentFieldName}/{recordPkId}` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/DownloadFileFromAttachmentTableField) |
| [Download View Attachment](actions/download-view-attachment.md) | `GET /v3/views/{viewName}/attachments/{attachmentFieldName}/{recordPkId}` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/DownloadFileFromAttachmentViewField) |
| [Get File Folder Metadata](actions/get-file-folder-metadata.md) | `GET /v3/files/folders/{externalKey}` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Files/GetFilesFolderMetadataByKey) |
| [Get File Metadata](actions/get-file-metadata.md) | `GET /v3/files/{externalKey}/fileInfo` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Files/GetFileMetadataByKey) |
| [Get Table](actions/get-table.md) | `GET /v3/tables/{tableName}` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/GetTable) |
| [Get Table Attachment Metadata](actions/get-table-attachment-metadata.md) | `GET /v3/tables/{tableName}/attachments/{attachmentFieldName}/fileInfo` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/GetFileMetadataFromAttachmentTableFields) |
| [Get Table Field](actions/get-table-field.md) | `GET /v3/tables/{tableName}/fields/{fieldName}` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/GetTableField) |
| [Get View](actions/get-view.md) | `GET /v3/views/{viewName}` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/GetView) |
| [Get View Attachment Metadata](actions/get-view-attachment-metadata.md) | `GET /v3/views/{viewName}/attachments/{attachmentFieldName}/fileInfo` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/GetFileMetadataFromAttachmentViewFields) |
| [Get View Field](actions/get-view-field.md) | `GET /v3/views/{viewName}/fields/{fieldName}` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/GetViewField) |
| [List File Folders](actions/list-file-folders.md) | `GET /v3/files/folders` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Files/ListFilesFolders) |
| [List Files](actions/list-files.md) | `GET /v3/files` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Files/ListFiles) |
| [List Table Fields](actions/list-table-fields.md) | `GET /v3/tables/{tableName}/fields` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/ListTableFields) |
| [List Table Records](actions/list-table-records.md) | `GET /v3/tables/{tableName}/records` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/ListTableRecords) |
| [List Tables](actions/list-tables.md) | `GET /v3/tables` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/ListTables) |
| [List View Fields](actions/list-view-fields.md) | `GET /v3/views/{viewName}/fields` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/ListViewFields) |
| [List View Records](actions/list-view-records.md) | `GET /v3/views/{viewName}/records` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/ListViewRecords) |
| [List Views](actions/list-views.md) | `GET /v3/views` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/ListViews) |
| [Rename Table Attachment](actions/rename-table-attachment.md) | `PUT /v3/tables/{tableName}/attachments/{attachmentFieldName}/fileInfo` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/UpdateFileMetadataInAttachmentTableFields) |
| [Rename View Attachment](actions/rename-view-attachment.md) | `PUT /v3/views/{viewName}/attachments/{attachmentFieldName}/fileInfo` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/UpdateFileMetadataInAttachmentViewFields) |
| [Update Table Records](actions/update-table-records.md) | `PUT /v3/tables/{tableName}/records` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/UpdateTableRecords) |
| [Update View Records](actions/update-view-records.md) | `PUT /v3/views/{viewName}/records` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/UpdateViewRecords) |
| [Upload Table Attachment](actions/upload-table-attachment.md) | `PUT /v3/tables/{tableName}/attachments/{attachmentFieldName}/{recordPkId}` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/UploadFileToAttachmentTableField) |
| [Upload View Attachment](actions/upload-view-attachment.md) | `PUT /v3/views/{viewName}/attachments/{attachmentFieldName}/{recordPkId}` | [docs](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Views/UploadFileToAttachmentViewField) |
