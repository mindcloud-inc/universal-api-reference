# Microsoft SharePoint Online: Native API Reference

A consolidated summary of Microsoft SharePoint Online's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/graph/api/resources/sharepoint?view=graph-rest-1.0
- **API base URL:** `https://graph.microsoft.com`

## Authentication

### OAuth 2.0

Connect with a Microsoft work or school account to access SharePoint through Microsoft Graph.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/organizations/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/organizations/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `offline_access User.Read Sites.Read.All Sites.ReadWrite.All Files.Read.All Files.ReadWrite.All`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/organizations/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/graph/auth-v2-user)

## Pagination

Use `$top` in the query string to set the page size (default 100; minimum 1). Use `$skiptoken` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | `POST /v1.0/drives/{{driveId}}/root/children` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-post-children?view=graph-rest-1.0) |
| [Create List Item](actions/create-list-item.md) | `POST /v1.0/sites/{{siteId}}/lists/{{listId}}/items` | [docs](https://learn.microsoft.com/en-us/graph/api/listitem-create?view=graph-rest-1.0) |
| [Delete Drive Item](actions/delete-drive-item.md) | `DELETE /v1.0/drives/{{driveId}}/items/{{itemId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-delete?view=graph-rest-1.0) |
| [Delete List Item](actions/delete-list-item.md) | `DELETE /v1.0/sites/{{siteId}}/lists/{{listId}}/items/{{itemId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/listitem-delete?view=graph-rest-1.0) |
| [Download File](actions/download-file.md) | `GET /v1.0/drives/{{driveId}}/items/{{itemId}}/content` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-get-content?view=graph-rest-1.0) |
| [Get Drive Item](actions/get-drive-item.md) | `GET /v1.0/drives/{{driveId}}/items/{{itemId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-get?view=graph-rest-1.0) |
| [Get List](actions/get-list.md) | `GET /v1.0/sites/{{siteId}}/lists/{{listId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/list-get?view=graph-rest-1.0) |
| [Get List Item](actions/get-list-item.md) | `GET /v1.0/sites/{{siteId}}/lists/{{listId}}/items/{{itemId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/listitem-get?view=graph-rest-1.0) |
| [Get Root Site](actions/get-root-site.md) | `GET /v1.0/sites/root` | [docs](https://learn.microsoft.com/en-us/graph/api/site-get?view=graph-rest-1.0) |
| [Get Site](actions/get-site.md) | `GET /v1.0/sites/{{siteId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/site-get?view=graph-rest-1.0) |
| [List Drive Root Items](actions/list-drive-root-items.md) | `GET /v1.0/drives/{{driveId}}/root/children` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-list-children?view=graph-rest-1.0) |
| [List Folder Items](actions/list-folder-items.md) | `GET /v1.0/drives/{{driveId}}/root:/{{folderPath}}:/children` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-list-children?view=graph-rest-1.0) |
| [List List Items](actions/list-list-items.md) | `GET /v1.0/sites/{{siteId}}/lists/{{listId}}/items` | [docs](https://learn.microsoft.com/en-us/graph/api/listitem-list?view=graph-rest-1.0) |
| [List Site Drives](actions/list-site-drives.md) | `GET /v1.0/sites/{{siteId}}/drives` | [docs](https://learn.microsoft.com/en-us/graph/api/drive-list?view=graph-rest-1.0) |
| [List Site Lists](actions/list-site-lists.md) | `GET /v1.0/sites/{{siteId}}/lists` | [docs](https://learn.microsoft.com/en-us/graph/api/list-list?view=graph-rest-1.0) |
| [Search Sites](actions/search-sites.md) | `GET /v1.0/sites` | [docs](https://learn.microsoft.com/en-us/graph/api/site-search?view=graph-rest-1.0) |
| [Upload File](actions/upload-file.md) | `PUT /v1.0/drives/{{driveId}}/root:/{{folderPath}}/{{fileName}}:/content` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-put-content?view=graph-rest-1.0) |
