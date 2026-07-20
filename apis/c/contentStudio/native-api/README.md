# ContentStudio: Native API Reference

A consolidated summary of ContentStudio's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://api-prod.contentstudio.io/guide
- **OpenAPI specification:** https://api-prod.contentstudio.io/api-docs.json
- **API base URL:** `https://api.contentstudio.io/api/v1`

## Authentication

### API Key

Authenticate with a ContentStudio API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://api-prod.contentstudio.io/guide)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment to Post](actions/add-comment-to-post.md) | `POST /workspaces/:workspace_id/posts/:post_id/comments` | [docs](https://api-prod.contentstudio.io/scalar) |
| [Approve or Reject Post](actions/approve-or-reject-post.md) | `POST /workspaces/:workspace_id/posts/:post_id/approval` | [docs](https://api-prod.contentstudio.io/scalar) |
| [Create Post](actions/create-post.md) | `POST /workspaces/:workspace_id/posts` | [docs](https://api-prod.contentstudio.io/scalar) |
| [Delete Post](actions/delete-post.md) | `DELETE /workspaces/:workspace_id/posts/:post_id` | [docs](https://api-prod.contentstudio.io/scalar) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /me` | [docs](https://api-prod.contentstudio.io/scalar) |
| [List Campaigns](actions/list-campaigns.md) | `GET /workspaces/:workspace_id/campaigns` | [docs](https://api-prod.contentstudio.io/scalar) |
| [List Content Categories](actions/list-content-categories.md) | `GET /workspaces/:workspace_id/content-categories` | [docs](https://api-prod.contentstudio.io/scalar) |
| [List Labels](actions/list-labels.md) | `GET /workspaces/:workspace_id/labels` | [docs](https://api-prod.contentstudio.io/scalar) |
| [List Media Assets](actions/list-media-assets.md) | `GET /workspaces/:workspace_id/media` | [docs](https://api-prod.contentstudio.io/scalar) |
| [List Post Comments](actions/list-post-comments.md) | `GET /workspaces/:workspace_id/posts/:post_id/comments` | [docs](https://api-prod.contentstudio.io/scalar) |
| [List Posts](actions/list-posts.md) | `GET /workspaces/:workspace_id/posts` | [docs](https://api-prod.contentstudio.io/scalar) |
| [List Social Accounts](actions/list-social-accounts.md) | `GET /workspaces/:workspace_id/accounts` | [docs](https://api-prod.contentstudio.io/scalar) |
| [List Team Members](actions/list-team-members.md) | `GET /workspaces/:workspace_id/team-members` | [docs](https://api-prod.contentstudio.io/scalar) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://api-prod.contentstudio.io/scalar) |
| [Upload Media](actions/upload-media.md) | `POST /workspaces/:workspace_id/media` | [docs](https://api-prod.contentstudio.io/scalar) |
