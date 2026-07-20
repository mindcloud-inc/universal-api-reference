# Zenkit: Native API Reference

A consolidated summary of Zenkit's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://app.zenkit.com/docs/api
- **API base URL:** `https://zenkit.com/api/v1`

## Authentication

### API Key

Connect with your Zenkit API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.zenkit.com/docs/api/overview/authentication)

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Element To List](actions/add-element-to-list.md) | `POST /lists/:listId/elements` | [docs](https://app.zenkit.com/docs/api/elements/post-api-v1-lists-listid-elements) |
| [Create Entry](actions/create-entry.md) | `POST /lists/:listId/entries` | [docs](https://app.zenkit.com/docs/api/entries/post-api-v1-lists-listid-entries) |
| [Create List Entry Comment](actions/create-list-entry-comment.md) | `POST /users/me/lists/:listAllId/entries/:listEntryAllId/activities` | [docs](https://app.zenkit.com/docs/api/activity/post-api-v1-users-me-lists-listallid-entries-listentryallid-activities) |
| [Create Workspace](actions/create-workspace.md) | `POST /workspaces` | [docs](https://app.zenkit.com/docs/api/workspaces/post-api-v1-workspaces) |
| [Delete Deprecated Entry](actions/delete-deprecated-entry.md) | `DELETE /lists/:listAllId/deprecated-entries/:entryAllId` | [docs](https://app.zenkit.com/docs/api/entries/delete-api-v1-lists-listallid-deprecated-entries-entryallid) |
| [Deprecate Workspace](actions/deprecate-workspace.md) | `DELETE /workspaces/:workspaceAllId` | [docs](https://app.zenkit.com/docs/api/workspaces/delete-api-v1-workspaces-workspaceallid) |
| [Edit List Properties](actions/edit-list-properties.md) | `PUT /lists/:listAllId` | [docs](https://app.zenkit.com/docs/api/lists/put-api-v1-lists-listallid) |
| [Filter Entries](actions/filter-entries.md) | `POST /lists/:listShortId/entries/filter` | [docs](https://app.zenkit.com/docs/api/entries/post-api-v1-lists-listshortid-entries-filter) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://app.zenkit.com/docs/api/users/get-api-v1-users-me) |
| [Get Elements In List](actions/get-elements-in-list.md) | `GET /lists/:listAllId/elements` | [docs](https://app.zenkit.com/docs/api/elements/get-api-v1-lists-listallid-elements) |
| [Get Entry](actions/get-entry.md) | `GET /lists/:listAllId/entries/:listEntryAllId` | [docs](https://app.zenkit.com/docs/api/entries/get-api-v1-lists-listallid-entries-listentryallid) |
| [Get Filtered Entries For List View](actions/get-filtered-entries-for-list-view.md) | `POST /lists/:listShortId/entries/filter/list` | [docs](https://app.zenkit.com/docs/api/entries/post-api-v1-lists-listshortid-entries-filter-list) |
| [Get List](actions/get-list.md) | `GET /lists/:listShortId` | [docs](https://app.zenkit.com/docs/api/lists/get-api-v1-lists-listshortid) |
| [Get Users For List](actions/get-users-for-list.md) | `GET /lists/:listAllId/users` | [docs](https://app.zenkit.com/docs/api/lists/get-api-v1-lists-listallid-users) |
| [Get Users For Workspace](actions/get-users-for-workspace.md) | `GET /workspaces/:workspaceId/users` | [docs](https://app.zenkit.com/docs/api/workspaces/get-api-v1-workspaces-workspaceid-users) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:workspaceAllId` | [docs](https://app.zenkit.com/docs/api/workspaces/get-api-v1-workspaces-workspaceallid) |
| [Get Workspaces And Lists](actions/get-workspaces-and-lists.md) | `GET /users/me/workspacesWithLists` | [docs](https://app.zenkit.com/docs/api/workspaces/get-api-v1-users-me-workspaceswithlists) |
| [Search Entries](actions/search-entries.md) | `GET /entries/search` | [docs](https://app.zenkit.com/docs/api/entries/get-api-v1-entries-search-query-limit-preferredlistids-excludelistentryuuids-searchinarchive-includerelatedlists-includerelatedworkspaces-includerelatedlistelements) |
| [Update Element In List](actions/update-element-in-list.md) | `PUT /lists/:listId/elements/:elementId` | [docs](https://app.zenkit.com/docs/api/elements/put-api-v1-lists-listid-elements-elementid) |
| [Update Entry](actions/update-entry.md) | `PUT /lists/:listId/entries/:listEntryId` | [docs](https://app.zenkit.com/docs/api/entries/put-api-v1-lists-listid-entries-listentryid) |
| [Update Entry Field](actions/update-entry-field.md) | `PUT /lists/:listId/entries/:listEntryId/elements/:elementId` | [docs](https://app.zenkit.com/docs/api/entries/put-api-v1-lists-listid-entries-listentryid-elements-elementid) |
| [Update Workspace Details](actions/update-workspace-details.md) | `PUT /workspaces/:workspaceAllId` | [docs](https://app.zenkit.com/docs/api/workspaces/put-api-v1-workspaces-workspaceallid) |
