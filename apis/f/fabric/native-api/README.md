# Fabric: Native API Reference

A consolidated summary of Fabric's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://developers.fabric.so/api-reference
- **API base URL:** `https://api.fabric.so`

## Authentication

### API Key

Fabric API uses the X-Api-Key header for authenticated requests.

### Credentials

- **API Key:** `apiKey` · required · Fabric API key used in the X-Api-Key header.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://developers.fabric.so/developer-guide/getting-started)

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Confirm Workspace Deletion](actions/confirm-workspace-deletion.md) | `POST /v2/workspaces/deletion-confirmation` | [docs](https://developers.fabric.so/api-reference/tag/workspaces/post/v2/workspaces/deletion-confirmation) |
| [Create Bookmark](actions/create-bookmark.md) | `POST /v2/bookmarks` | [docs](https://developers.fabric.so/api-reference/tag/bookmarks/post/v2/bookmarks) |
| [Create File](actions/create-file.md) | `POST /v2/files` | [docs](https://developers.fabric.so/api-reference/tag/files/post/v2/files) |
| [Create Folder](actions/create-folder.md) | `POST /v2/folders` | [docs](https://developers.fabric.so/api-reference/tag/folders/post/v2/folders) |
| [Create Memory](actions/create-memory.md) | `POST /v2/memories` | [docs](https://developers.fabric.so/api-reference/tag/memories/post/v2/memories) |
| [Create Notepad](actions/create-notepad.md) | `POST /v2/notepads` | [docs](https://developers.fabric.so/api-reference/tag/notepads/post/v2/notepads) |
| [Create Space](actions/create-space.md) | `POST /v2/spaces` | [docs](https://developers.fabric.so/api-reference/tag/spaces/post/v2/spaces) |
| [Create Tag](actions/create-tag.md) | `POST /v2/tags` | [docs](https://developers.fabric.so/api-reference/tag/tags/post/v2/tags) |
| [Create Workspace](actions/create-workspace.md) | `POST /v2/workspaces` | [docs](https://developers.fabric.so/api-reference/tag/workspaces/post/v2/workspaces) |
| [Delete Memory](actions/delete-memory.md) | `DELETE /v2/memories/{memoryId}` | [docs](https://developers.fabric.so/api-reference/tag/memories/delete/v2/memories/memoryId) |
| [Delete Resources](actions/delete-resources.md) | `POST /v2/resources/delete` | [docs](https://developers.fabric.so/api-reference/tag/resources/post/v2/resources/delete) |
| [Delete Space](actions/delete-space.md) | `DELETE /v2/spaces/{spaceId}` | [docs](https://developers.fabric.so/api-reference/tag/spaces/delete/v2/spaces/spaceId) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /v2/workspaces` | [docs](https://developers.fabric.so/api-reference/tag/workspaces/delete/v2/workspaces) |
| [Get Memory](actions/get-memory.md) | `GET /v2/memories/{memoryId}` | [docs](https://developers.fabric.so/api-reference/tag/memories/get/v2/memories/memoryId) |
| [Get Memory Job](actions/get-memory-job.md) | `GET /v2/memories/jobs/{jobId}` | [docs](https://developers.fabric.so/api-reference/tag/memories/get/v2/memories/jobs/jobId) |
| [Get My Profile](actions/get-my-profile.md) | `GET /v2/users/me` | [docs](https://developers.fabric.so/api-reference/tag/users/get/v2/users/me) |
| [Get Notepad Content](actions/get-notepad-content.md) | `GET /v2/notepads/{resourceId}/content` | [docs](https://developers.fabric.so/api-reference/tag/notepads/get/v2/notepads/resourceId/content) |
| [Get Resource](actions/get-resource.md) | `GET /v2/resources/{resourceId}` | [docs](https://developers.fabric.so/api-reference/tag/resources/get/v2/resources/resourceId) |
| [Get Resource Root](actions/get-resource-root.md) | `GET /v2/resource-roots/{resourceRootId}` | [docs](https://developers.fabric.so/api-reference/tag/resource-roots/get/v2/resource-roots/resourceRootId) |
| [Get Upload URL](actions/get-upload-url.md) | `GET /v2/upload` | [docs](https://developers.fabric.so/api-reference/tag/uploads/get/v2/upload) |
| [Get User Subscription](actions/get-user-subscription.md) | `GET /v2/subscriptions` | [docs](https://developers.fabric.so/api-reference/tag/subscriptions/get/v2/subscriptions) |
| [Get Workspace](actions/get-workspace.md) | `GET /v2/workspaces/me` | [docs](https://developers.fabric.so/api-reference/tag/workspaces/get/v2/workspaces/me) |
| [List Comments](actions/list-comments.md) | `GET /v2/resources/{resourceId}/comments` | [docs](https://developers.fabric.so/api-reference/tag/comments/get/v2/resources/resourceId/comments) |
| [List Resource Roots](actions/list-resource-roots.md) | `GET /v2/resource-roots` | [docs](https://developers.fabric.so/api-reference/tag/resource-roots/get/v2/resource-roots) |
| [List Resources](actions/list-resources.md) | `POST /v2/resources/filter` | [docs](https://developers.fabric.so/api-reference/tag/resources/post/v2/resources/filter) |
| [List Spaces](actions/list-spaces.md) | `GET /v2/spaces` | [docs](https://developers.fabric.so/api-reference/tag/spaces/get/v2/spaces) |
| [List Tags](actions/list-tags.md) | `GET /v2/tags` | [docs](https://developers.fabric.so/api-reference/tag/tags/get/v2/tags) |
| [List Workspaces](actions/list-workspaces.md) | `GET /v2/workspaces` | [docs](https://developers.fabric.so/api-reference/tag/workspaces/get/v2/workspaces) |
| [Recover Resources](actions/recover-resources.md) | `POST /v2/resources/recover` | [docs](https://developers.fabric.so/api-reference/tag/resources/post/v2/resources/recover) |
| [Reorder Resources](actions/reorder-resources.md) | `PATCH /v2/resources/position` | [docs](https://developers.fabric.so/api-reference/tag/resources/patch/v2/resources/position) |
| [Search](actions/search.md) | `POST /v2/search` | [docs](https://developers.fabric.so/api-reference/tag/search/post/v2/search) |
| [Search Memories](actions/search-memories.md) | `GET /v2/memories/search` | [docs](https://developers.fabric.so/api-reference/tag/memories/get/v2/memories/search) |
| [Update Memory](actions/update-memory.md) | `PATCH /v2/memories/{memoryId}` | [docs](https://developers.fabric.so/api-reference/tag/memories/patch/v2/memories/memoryId) |
| [Update Resource](actions/update-resource.md) | `PATCH /v2/resources/{resourceId}` | [docs](https://developers.fabric.so/api-reference/tag/resources/patch/v2/resources/resourceId) |
| [Update Workspace](actions/update-workspace.md) | `PATCH /v2/workspaces` | [docs](https://developers.fabric.so/api-reference/tag/workspaces/patch/v2/workspaces) |
