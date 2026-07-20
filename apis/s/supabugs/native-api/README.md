# Supabugs: Native API Reference

A consolidated summary of Supabugs's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://api.supabugs.io/api/public/v1/docs/index.html
- **OpenAPI specification:** https://api.supabugs.io/api/public/v1/docs/doc.json
- **API base URL:** `https://api.supabugs.io/api/public/v1`

## Authentication

### API Token

Use a Supabugs API token for project-scoped API access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.supabugs.io/api/public/v1/docs/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Issue Comment](actions/add-issue-comment.md) | `POST /issues/:id/comments` | [docs](https://api.supabugs.io/api/public/v1/docs/index.html) |
| [Create Issue](actions/create-issue.md) | `POST /issues` | [docs](https://api.supabugs.io/api/public/v1/docs/index.html) |
| [Delete Issue](actions/delete-issue.md) | `DELETE /issues/:id` | [docs](https://api.supabugs.io/api/public/v1/docs/index.html) |
| [Delete Issue Attachment](actions/delete-issue-attachment.md) | `DELETE /issues/:issueId/attachments/:id` | [docs](https://api.supabugs.io/api/public/v1/docs/index.html) |
| [Delete Issue Comment](actions/delete-issue-comment.md) | `DELETE /issues/:issueId/comments/:id` | [docs](https://api.supabugs.io/api/public/v1/docs/index.html) |
| [Get Issue](actions/get-issue.md) | `GET /issues/:id` | [docs](https://api.supabugs.io/api/public/v1/docs/index.html) |
| [Get Project](actions/get-project.md) | `GET /project` | [docs](https://api.supabugs.io/api/public/v1/docs/index.html) |
| [List Issues](actions/list-issues.md) | `GET /issues` | [docs](https://api.supabugs.io/api/public/v1/docs/index.html) |
| [List Lookup Values](actions/list-lookup-values.md) | `GET /lov` | [docs](https://api.supabugs.io/api/public/v1/docs/index.html) |
| [Search Issues](actions/search-issues.md) | `POST /issues/search` | [docs](https://api.supabugs.io/api/public/v1/docs/index.html) |
| [Update Issue](actions/update-issue.md) | `PUT /issues/:id` | [docs](https://api.supabugs.io/api/public/v1/docs/index.html) |
| [Upload Issue Attachment](actions/upload-issue-attachment.md) | `POST /issues/:id/upload-attachments` | [docs](https://api.supabugs.io/api/public/v1/docs/index.html) |
