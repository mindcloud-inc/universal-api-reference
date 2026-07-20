# Mendeley: Native API Reference

A consolidated summary of Mendeley's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://dev.mendeley.com/
- **API base URL:** `https://api.mendeley.com`

## Authentication

### OAuth 2.0

Connect a Mendeley developer application using OAuth 2.0 Authorization Code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.mendeley.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.mendeley.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `all`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.mendeley.com/oauth/token.

[Official authentication documentation](https://dev.mendeley.com/reference/topics/authorization_auth_code.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–500). Use `marker` in the query string as the pagination cursor.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Document To Folder](actions/add-document-to-folder.md) | `POST /folders/:id/documents` | [docs](https://dev.mendeley.com/methods/#adding-a-document-to-a-folder) |
| [Create Annotation](actions/create-annotation.md) | `POST /annotations` | [docs](https://dev.mendeley.com/methods/#creating-an-annotation) |
| [Create Document](actions/create-document.md) | `POST /documents` | [docs](https://dev.mendeley.com/methods/#creating-a-document-from-metadata) |
| [Create Folder](actions/create-folder.md) | `POST /folders` | [docs](https://dev.mendeley.com/methods/#creating-a-folder) |
| [Delete Annotation](actions/delete-annotation.md) | `DELETE /annotations/:id` | [docs](https://dev.mendeley.com/methods/#deleting-an-annotation) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /folders/:id` | [docs](https://dev.mendeley.com/methods/#deleting-a-folder) |
| [Delete Trashed Document](actions/delete-trashed-document.md) | `DELETE /trash/:id` | [docs](https://dev.mendeley.com/methods/#deleting-a-trashed-document) |
| [Get BibTeX Document](actions/get-bibtex-document.md) | `GET /documents/:id` | [docs](https://dev.mendeley.com/methods/#retrieving-a-bibtex-document) |
| [Get Catalog Document](actions/get-catalog-document.md) | `GET /catalog/:id` | [docs](https://dev.mendeley.com/methods/#retrieving-a-catalog-document) |
| [Get Document](actions/get-document.md) | `GET /documents/:id` | [docs](https://dev.mendeley.com/methods/#retrieving-a-document) |
| [Get My Profile](actions/get-my-profile.md) | `GET /profiles/me` | [docs](https://dev.mendeley.com/methods/) |
| [Get Trashed Document](actions/get-trashed-document.md) | `GET /trash/:id` | [docs](https://dev.mendeley.com/methods/#retrieve-a-trashed-document) |
| [List Annotations](actions/list-annotations.md) | `GET /annotations` | [docs](https://dev.mendeley.com/methods/#retrieving-annotations) |
| [List BibTeX Documents](actions/list-bibtex-documents.md) | `GET /documents` | [docs](https://dev.mendeley.com/methods/#retrieving-bibtex-documents) |
| [List Catalog Documents](actions/list-catalog-documents.md) | `GET /catalog` | [docs](https://dev.mendeley.com/methods/#retrieving-catalog-documents) |
| [List Documents](actions/list-documents-stage3.md) | `GET /documents` | [docs](https://dev.mendeley.com/methods/#retrieving-documents) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://dev.mendeley.com/methods/#retrieving-files) |
| [List Folder Documents](actions/list-folder-documents.md) | `GET /folders/:id/documents` | [docs](https://dev.mendeley.com/methods/#retrieving-documents-in-a-folder) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://dev.mendeley.com/methods/#list-all-folders) |
| [List Trashed Documents](actions/list-trashed-documents.md) | `GET /trash` | [docs](https://dev.mendeley.com/methods/#retrieve-all-trashed-documents) |
| [Metadata Lookup](actions/metadata-lookup.md) | `GET /metadata` | [docs](https://dev.mendeley.com/methods/#metadata-lookup) |
| [Remove Document From Folder](actions/remove-document-from-folder.md) | `DELETE /folders/:id/documents/:document_id` | [docs](https://dev.mendeley.com/methods/#deleting-a-document-from-a-folder) |
| [Restore Document](actions/restore-document.md) | `POST /trash/:id/restore` | [docs](https://dev.mendeley.com/methods/#restoring-a-document) |
| [Trash Document](actions/trash-document.md) | `POST /documents/:id/trash` | [docs](https://dev.mendeley.com/methods/#move-a-document-to-the-trash) |
| [Update Annotation](actions/update-annotation.md) | `PATCH /annotations/:id` | [docs](https://dev.mendeley.com/methods/#updating-an-annotation) |
| [Update Document](actions/update-document.md) | `PATCH /documents/:id` | [docs](https://dev.mendeley.com/methods/#updating-documents) |
| [Update Folder](actions/update-folder.md) | `PATCH /folders/:id` | [docs](https://dev.mendeley.com/methods/#updating-a-folder) |
| [Update My Profile](actions/update-my-profile.md) | `PATCH /profiles/me` | [docs](https://dev.mendeley.com/methods/#updating-the-logged-in-user%27s-profile) |
