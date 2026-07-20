# Dovetail: Native API Reference

A consolidated summary of Dovetail's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://developers.dovetail.com/reference
- **API base URL:** `https://dovetail.com/api`

## Authentication

### API Key

Connect with a Dovetail personal API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.dovetail.com/reference/authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page[limit]` in the query string to set the page size. Use `page[start_cursor]` in the query string as the pagination cursor.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /v1/contacts` | [docs](https://developers.dovetail.com/reference/post_v1-contacts) |
| [Create Data](actions/create-data.md) | `POST /v1/data` | [docs](https://developers.dovetail.com/reference/post_v1-data) |
| [Create Doc](actions/create-doc.md) | `POST /v1/docs` | [docs](https://developers.dovetail.com/reference/post_v1-docs) |
| [Create Folder](actions/create-folder.md) | `POST /v1/folders` | [docs](https://developers.dovetail.com/reference/post_v1-folders) |
| [Create Project](actions/create-project.md) | `POST /v1/projects` | [docs](https://developers.dovetail.com/reference/post_v1-projects) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v1/contacts/:contactId` | [docs](https://developers.dovetail.com/reference/delete_v1-contacts-contactid) |
| [Delete Data](actions/delete-data.md) | `DELETE /v1/data/:dataId` | [docs](https://developers.dovetail.com/reference/delete_v1-data-data_id) |
| [Delete Doc](actions/delete-doc.md) | `DELETE /v1/docs/:docId` | [docs](https://developers.dovetail.com/reference/delete_v1-docs-doc_id) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /v1/folders/:folderId` | [docs](https://developers.dovetail.com/reference/delete_v1-folders-folderid) |
| [Delete Project](actions/delete-project.md) | `DELETE /v1/projects/:projectId` | [docs](https://developers.dovetail.com/reference/delete_v1-projects-projectid) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contacts/:contactId` | [docs](https://developers.dovetail.com/reference/get_v1-contacts-contactid) |
| [Get Data](actions/get-data.md) | `GET /v1/data/:dataId` | [docs](https://developers.dovetail.com/reference/get_v1-data-data_id) |
| [Get Doc](actions/get-doc.md) | `GET /v1/docs/:docId` | [docs](https://developers.dovetail.com/reference/get_v1-docs-docid) |
| [Get Folder](actions/get-folder.md) | `GET /v1/folders/:folderId` | [docs](https://developers.dovetail.com/reference/get_v1-folders-folderid) |
| [Get Project](actions/get-project.md) | `GET /v1/projects/:projectId` | [docs](https://developers.dovetail.com/reference/get_v1-projects-projectid) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts` | [docs](https://developers.dovetail.com/reference/get_v1-contacts) |
| [List Data](actions/list-data.md) | `GET /v1/data` | [docs](https://developers.dovetail.com/reference/get_v1-data) |
| [List Docs](actions/list-docs.md) | `GET /v1/docs` | [docs](https://developers.dovetail.com/reference/get_v1-docs) |
| [List Folders](actions/list-folders.md) | `GET /v1/folders` | [docs](https://developers.dovetail.com/reference/get_v1-folders) |
| [List Projects](actions/list-projects.md) | `GET /v1/projects` | [docs](https://developers.dovetail.com/reference/get_v1-projects) |
| [Update Contact](actions/update-contact.md) | `PATCH /v1/contacts/:contactId` | [docs](https://developers.dovetail.com/reference/patch_v1-contacts-contactid) |
| [Update Data](actions/update-data.md) | `PATCH /v1/data/:dataId` | [docs](https://developers.dovetail.com/reference/patch_v1-data-data_id) |
| [Update Doc](actions/update-doc.md) | `PATCH /v1/docs/:docId` | [docs](https://developers.dovetail.com/reference/patch_v1-docs-docid) |
| [Update Folder](actions/update-folder.md) | `PATCH /v1/folders/:folderId` | [docs](https://developers.dovetail.com/reference/patch_v1-folders-folderid) |
| [Update Project](actions/update-project.md) | `PATCH /v1/projects/:projectId` | [docs](https://developers.dovetail.com/reference/patch_v1-projects-projectid) |
