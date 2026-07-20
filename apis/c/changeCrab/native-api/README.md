# ChangeCrab: Native API Reference

A consolidated summary of ChangeCrab's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://changecrab.com/api/documentation
- **API base URL:** `https://changecrab.com/api`

## Authentication

### API Key

Authenticate ChangeCrab with the API key from ChangeCrab account settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://changecrab.com/api/documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Changelog](actions/create-changelog.md) | `POST /changelogs` | [docs](https://changecrab.com/knowledge-base/integrations/api-create-changelog) |
| [Create Post](actions/create-post.md) | `POST /changelogs/:id/posts` | [docs](https://changecrab.com/knowledge-base/integrations/api-manage-posts) |
| [Delete Changelog](actions/delete-changelog.md) | `DELETE /changelogs/:id` | [docs](https://changecrab.com/knowledge-base/integrations/api-overview) |
| [Delete Post](actions/delete-post.md) | `DELETE /changelogs/:id/posts/:postId` | [docs](https://changecrab.com/knowledge-base/integrations/api-manage-posts) |
| [Get Changelog](actions/get-changelog.md) | `GET /changelogs/:id` | [docs](https://changecrab.com/knowledge-base/integrations/api-overview) |
| [List Categories](actions/list-categories.md) | `GET /changelogs/:id/categories` | [docs](https://changecrab.com/knowledge-base/integrations/api-overview) |
| [List Changelogs](actions/list-changelogs.md) | `GET /changelogs` | [docs](https://changecrab.com/knowledge-base/integrations/api-overview) |
| [List Posts](actions/list-posts.md) | `GET /changelogs/:id/posts` | [docs](https://changecrab.com/knowledge-base/integrations/api-manage-posts) |
| [Update Changelog](actions/update-changelog.md) | `PUT /changelogs/:id` | [docs](https://changecrab.com/knowledge-base/integrations/api-overview) |
| [Update Post](actions/update-post.md) | `PUT /changelogs/:id/posts/:postId` | [docs](https://changecrab.com/knowledge-base/integrations/api-manage-posts) |
