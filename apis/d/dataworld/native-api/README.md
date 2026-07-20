# data.world: Native API Reference

A consolidated summary of data.world's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.data.world/docs/data-world-for-developers/
- **API base URL:** `https://api.data.world/v0`

## Authentication

### API Token

Authenticate to data.world using a user API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.data.world/docs/api-getting-started)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Files from URLs](actions/add-files-from-urls.md) | `POST /datasets/{owner}/{id}/files` | [docs](https://developer.data.world/reference/addfilesbysource-1) |
| [Create a Dataset](actions/create-dataset.md) | `POST /datasets/{owner}` | [docs](https://developer.data.world/reference/createdataset-1) |
| [Create a Data Project](actions/create-project.md) | `POST /projects/{owner}` | [docs](https://developer.data.world/reference/createproject-1) |
| [Delete a Dataset](actions/delete-dataset.md) | `DELETE /datasets/{owner}/{id}` | [docs](https://developer.data.world/reference/deletedataset-1) |
| [Delete Files](actions/delete-files.md) | `DELETE /datasets/{owner}/{id}/files` | [docs](https://developer.data.world/reference/deletefilesandsyncsources-1) |
| [Delete a Data Project](actions/delete-project.md) | `DELETE /projects/{owner}/{id}` | [docs](https://developer.data.world/reference/deleteproject-1) |
| [Describe a SQL Query](actions/describe-sql-query.md) | `POST /sql/{owner}/{id}/describe` | [docs](https://developer.data.world/reference/sqldescribe-1) |
| [Download a Dataset](actions/download-dataset.md) | `GET /download/{owner}/{id}` | [docs](https://developer.data.world/reference/downloaddataset-1) |
| [Download a File](actions/download-file.md) | `GET /file_download/{owner}/{id}/{file}` | [docs](https://developer.data.world/reference/downloadfile-1) |
| [Execute a Saved Query](actions/execute-saved-query.md) | `GET /queries/{id}/results` | [docs](https://developer.data.world/reference/executequery-1) |
| [Execute a Saved Query (with Parameters)](actions/execute-saved-query-with-parameters.md) | `POST /queries/{id}/results` | [docs](https://developer.data.world/reference/executequerywithpost-1) |
| [Get File Description and Labels](actions/get-file-metadata.md) | `GET /datasets/{owner}/{id}/files/{file}/metadata` | [docs](https://developer.data.world/reference/getfilemetadata-1) |
| [Link Dataset](actions/link-dataset.md) | `PUT /projects/{owner}/{id}/linkedDatasets/{linkedDatasetOwner}/{linkedDatasetId}` | [docs](https://developer.data.world/reference/addlinkeddataset-1) |
| [List Datasets for Owner](actions/list-datasets-for-owner.md) | `GET /datasets/{owner}` | [docs](https://developer.data.world/reference/getdatasetsbyowner-1) |
| [List Projects for Owner](actions/list-projects-for-owner.md) | `GET /projects/{owner}` | [docs](https://developer.data.world/reference/getprojectsbyowner-1) |
| [List User Saved Queries](actions/list-user-saved-queries.md) | `GET /datasets/{owner}/{id}/userQueries` | [docs](https://developer.data.world/reference/getusersaveddatasetqueries) |
| [Create / Replace a Dataset](actions/replace-dataset.md) | `PUT /datasets/{owner}/{id}` | [docs](https://developer.data.world/reference/replacedataset-1) |
| [Retrieve Dataset](actions/retrieve-dataset.md) | `GET /datasets/{owner}/{id}` | [docs](https://developer.data.world/reference/getdataset-1) |
| [Retrieve a Dataset Version](actions/retrieve-dataset-version.md) | `GET /datasets/{owner}/{id}/v/{versionId}` | [docs](https://developer.data.world/reference/getdatasetbyversion-1) |
| [Retrieve Project](actions/retrieve-project.md) | `GET /projects/{owner}/{id}` | [docs](https://developer.data.world/reference/getproject-1) |
| [Retrieve a Data Project Version](actions/retrieve-project-version.md) | `GET /projects/{owner}/{id}/v/{versionId}` | [docs](https://developer.data.world/reference/getprojectbyversion-1) |
| [SQL Query](actions/sql-query.md) | `POST /sql/{owner}/{id}` | [docs](https://developer.data.world/reference/sqlpostwithjsonrequest-1) |
| [Sync Files](actions/sync-files.md) | `POST /datasets/{owner}/{id}/sync` | [docs](https://developer.data.world/reference/sync-1) |
| [Sync Files (via GET)](actions/sync-files-via-get.md) | `GET /datasets/{owner}/{id}/sync` | [docs](https://developer.data.world/reference/syncviaget-1) |
| [Unlink Dataset](actions/unlink-dataset.md) | `DELETE /projects/{owner}/{id}/linkedDatasets/{linkedDatasetOwner}/{linkedDatasetId}` | [docs](https://developer.data.world/reference/removelinkeddataset-1) |
| [Update a Dataset](actions/update-dataset.md) | `PATCH /datasets/{owner}/{id}` | [docs](https://developer.data.world/reference/patchdataset-1) |
| [Update File Description and Labels](actions/update-file-metadata.md) | `PATCH /datasets/{owner}/{id}/files/{file}/metadata` | [docs](https://developer.data.world/reference/patchfilemetadata-1) |
| [Update a Data Project](actions/update-project.md) | `PATCH /projects/{owner}/{id}` | [docs](https://developer.data.world/reference/patchproject-1) |
| [Upload a File](actions/upload-file.md) | `PUT /uploads/{owner}/{id}/files/{file}` | [docs](https://developer.data.world/reference/uploadfile-1) |
| [Upload Files](actions/upload-files.md) | `POST /uploads/{owner}/{id}/files` | [docs](https://developer.data.world/reference/uploadfiles-1) |
