# Blaze AI: Native API Reference

A consolidated summary of Blaze AI's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://api.blaze.ai/api/documentation
- **OpenAPI specification:** https://api.blaze.ai/api/v1/open_api_doc
- **API base URL:** `https://api.blaze.ai`

## Authentication

### API Key

Use a Blaze AI API access token. Blaze expects the token in the Authorization header as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.blaze.ai/api/documentation)

## Pagination

Use `items` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Doc Access](actions/add-doc-access.md) | `POST /api/v1/w/:workspace_id/docs/:doc_id/accesses` | [docs](https://api.blaze.ai/api/documentation#!/accesses/postApiV1WWorkspaceIdDocsDocIdAccesses) |
| [Add Doc Property](actions/add-doc-property.md) | `POST /api/v1/w/:workspace_id/docs/:doc_id/properties` | [docs](https://api.blaze.ai/api/documentation#!/properties/postApiV1WWorkspaceIdDocsDocIdProperties) |
| [Add Handbook Item](actions/add-handbook-item.md) | `POST /api/v1/w/:workspace_id/handbooks/:handbook_id/items` | [docs](https://api.blaze.ai/api/documentation#!/handbook%20items/postApiV1WWorkspaceIdHandbooksHandbookIdItems) |
| [Create Folder](actions/create-folder.md) | `POST /api/v1/w/:workspace_id/folders` | [docs](https://api.blaze.ai/api/documentation#!/folders/postApiV1WWorkspaceIdFolders) |
| [Create Published Doc Subscription](actions/create-published-doc-subscription.md) | `POST /api/v1/w/:workspace_id/published_doc_subscriptions` | [docs](https://api.blaze.ai/api/documentation#!/subscriptions/postApiV1WWorkspaceIdPublishedDocSubscriptions) |
| [Create Workspace Property](actions/create-workspace-property.md) | `POST /api/v1/w/:workspace_id/properties` | [docs](https://api.blaze.ai/api/documentation#!/properties/postApiV1WWorkspaceIdProperties) |
| [Delete Handbook Item](actions/delete-handbook-item.md) | `DELETE /api/v1/w/:workspace_id/handbooks/:handbook_id/items/:id` | [docs](https://api.blaze.ai/api/documentation#!/handbook%20items/deleteApiV1WWorkspaceIdHandbooksHandbookIdItemsId) |
| [Delete Published Doc Subscription](actions/delete-published-doc-subscription.md) | `DELETE /api/v1/w/:workspace_id/published_doc_subscriptions/:id` | [docs](https://api.blaze.ai/api/documentation#!/subscriptions/deleteApiV1WWorkspaceIdPublishedDocSubscriptionsId) |
| [Delete Workspace Property](actions/delete-workspace-property.md) | `DELETE /api/v1/w/:workspace_id/properties/:id` | [docs](https://api.blaze.ai/api/documentation#!/properties/deleteApiV1WWorkspaceIdPropertiesId) |
| [Generate Doc](actions/generate-doc.md) | `POST /api/v1/w/:workspace_id/docs/ai-generation` | [docs](https://api.blaze.ai/api/documentation#!/docs/postApiV1WWorkspaceIdDocsAiGeneration) |
| [Get Doc](actions/get-doc.md) | `GET /api/v1/w/:workspace_id/docs/:id` | [docs](https://api.blaze.ai/api/documentation#!/docs/getApiV1WWorkspaceIdDocsId) |
| [Get Folder](actions/get-folder.md) | `GET /api/v1/w/:workspace_id/folders/:id` | [docs](https://api.blaze.ai/api/documentation#!/folders/getApiV1WWorkspaceIdFoldersId) |
| [Get Import](actions/get-import.md) | `GET /api/v1/w/:workspace_id/imports/:id` | [docs](https://api.blaze.ai/api/documentation#!/imports/getApiV1WWorkspaceIdImportsId) |
| [Get Published Docs Polling Test](actions/get-published-docs-polling-test.md) | `GET /api/v1/w/:workspace_id/zapier_published_docs_polling_test` | [docs](https://api.blaze.ai/api/documentation#!/w/getApiV1WWorkspaceIdZapierPublishedDocsPollingTest) |
| [Import Doc](actions/import-doc.md) | `POST /api/v1/w/:workspace_id/imports` | [docs](https://api.blaze.ai/api/documentation#!/imports/postApiV1WWorkspaceIdImports) |
| [List Brand Voices](actions/list-brand-voices.md) | `GET /api/v1/w/:workspace_id/brand_voices` | [docs](https://api.blaze.ai/api/documentation#!/brand_voices/getApiV1WWorkspaceIdBrandVoices) |
| [List Doc Accesses](actions/list-doc-accesses.md) | `GET /api/v1/w/:workspace_id/docs/:doc_id/accesses` | [docs](https://api.blaze.ai/api/documentation#!/accesses/getApiV1WWorkspaceIdDocsDocIdAccesses) |
| [List Doc Properties](actions/list-doc-properties.md) | `GET /api/v1/w/:workspace_id/docs/:doc_id/properties` | [docs](https://api.blaze.ai/api/documentation#!/properties/getApiV1WWorkspaceIdDocsDocIdProperties) |
| [List Docs](actions/list-docs.md) | `GET /api/v1/w/:workspace_id/docs` | [docs](https://api.blaze.ai/api/documentation#!/docs/getApiV1WWorkspaceIdDocs) |
| [List Folders](actions/list-folders.md) | `GET /api/v1/w/:workspace_id/folders` | [docs](https://api.blaze.ai/api/documentation#!/folders/getApiV1WWorkspaceIdFolders) |
| [List Group Users](actions/list-group-users.md) | `GET /api/v1/w/:workspace_id/groups/:group_id/users` | [docs](https://api.blaze.ai/api/documentation#!/users/getApiV1WWorkspaceIdGroupsGroupIdUsers) |
| [List Groups](actions/list-groups.md) | `GET /api/v1/w/:workspace_id/groups` | [docs](https://api.blaze.ai/api/documentation#!/groups/getApiV1WWorkspaceIdGroups) |
| [List Handbook Items](actions/list-handbook-items.md) | `GET /api/v1/w/:workspace_id/handbooks/:handbook_id/items` | [docs](https://api.blaze.ai/api/documentation#!/handbook%20items/getApiV1WWorkspaceIdHandbooksHandbookIdItems) |
| [List Handbooks](actions/list-handbooks.md) | `GET /api/v1/w/:workspace_id/handbooks` | [docs](https://api.blaze.ai/api/documentation#!/handbooks/getApiV1WWorkspaceIdHandbooks) |
| [List Users](actions/list-users.md) | `GET /api/v1/w/:workspace_id/users` | [docs](https://api.blaze.ai/api/documentation#!/users/getApiV1WWorkspaceIdUsers) |
| [List Workspace Properties](actions/list-workspace-properties.md) | `GET /api/v1/w/:workspace_id/properties` | [docs](https://api.blaze.ai/api/documentation#!/properties/getApiV1WWorkspaceIdProperties) |
| [List Workspaces](actions/list-workspaces.md) | `GET /api/v1/w` | [docs](https://api.blaze.ai/api/documentation#!/w/getApiV1W) |
| [Move Files](actions/move-files.md) | `POST /api/v1/w/:workspace_id/files/move` | [docs](https://api.blaze.ai/api/documentation#!/files/postApiV1WWorkspaceIdFilesMove) |
| [Remove Doc Access](actions/remove-doc-access.md) | `DELETE /api/v1/w/:workspace_id/docs/:doc_id/accesses/:id` | [docs](https://api.blaze.ai/api/documentation#!/accesses/deleteApiV1WWorkspaceIdDocsDocIdAccessesId) |
| [Remove Doc Property](actions/remove-doc-property.md) | `DELETE /api/v1/w/:workspace_id/docs/:doc_id/properties/:id` | [docs](https://api.blaze.ai/api/documentation#!/properties/deleteApiV1WWorkspaceIdDocsDocIdPropertiesId) |
| [Update Doc](actions/update-doc.md) | `PATCH /api/v1/w/:workspace_id/docs/:id` | [docs](https://api.blaze.ai/api/documentation#!/docs/patchApiV1WWorkspaceIdDocsId) |
| [Update Doc Access](actions/update-doc-access.md) | `PATCH /api/v1/w/:workspace_id/docs/:doc_id/accesses/:id` | [docs](https://api.blaze.ai/api/documentation#!/accesses/patchApiV1WWorkspaceIdDocsDocIdAccessesId) |
| [Update Folder](actions/update-folder.md) | `PATCH /api/v1/w/:workspace_id/folders/:id` | [docs](https://api.blaze.ai/api/documentation#!/folders/patchApiV1WWorkspaceIdFoldersId) |
