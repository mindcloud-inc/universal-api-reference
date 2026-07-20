# Confluence: Native API Reference

A consolidated summary of Confluence's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.atlassian.com/cloud/confluence/rest/v2/intro/
- **OpenAPI specification:** https://dac-static.atlassian.com/cloud/confluence/openapi-v2.v3.json?_v=1.8489.0
- **API base URL:** `https://api.atlassian.com`

## Authentication

### OAuth 2.0

Connect Confluence Cloud with Atlassian OAuth 2.0 (3LO).

### Credentials

- **Cloud ID:** `cloudId` · optional · Optional Confluence cloud ID for site-specific actions. Run List Accessible Resources after connecting to find it.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.atlassian.com/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://auth.atlassian.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `delete:comment:confluence delete:page:confluence offline_access read:attachment:confluence read:comment:confluence read:content-details:confluence read:page:confluence read:space:confluence read:task:confluence write:attachment:confluence write:comment:confluence write:page:confluence write:space:confluence write:task:confluence`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://auth.atlassian.com/oauth/token.

[Official authentication documentation](https://developer.atlassian.com/cloud/confluence/oauth-2-3lo-apps/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–250). Use `cursor` in the query string as the pagination cursor.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Attachment For Page](actions/create-attachment-for-page.md) | `POST /ex/confluence/:cloudId/wiki/rest/api/content/:id/child/attachment` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v1/api-group-content---attachments/) |
| [Create Blog Post](actions/create-blog-post.md) | `POST /ex/confluence/:cloudId/wiki/api/v2/blogposts` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-blog-post/) |
| [Create Footer Comment](actions/create-footer-comment.md) | `POST /ex/confluence/:cloudId/wiki/api/v2/footer-comments` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-comment/) |
| [Create Page](actions/create-page.md) | `POST /ex/confluence/:cloudId/wiki/api/v2/pages` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-page/) |
| [Delete Blog Post](actions/delete-blog-post.md) | `DELETE /ex/confluence/:cloudId/wiki/api/v2/blogposts/:id` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-blog-post/) |
| [Delete Footer Comment](actions/delete-footer-comment.md) | `DELETE /ex/confluence/:cloudId/wiki/api/v2/footer-comments/:commentId` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-comment/) |
| [Delete Page](actions/delete-page.md) | `DELETE /ex/confluence/:cloudId/wiki/api/v2/pages/:id` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-page/) |
| [Get Attachment](actions/get-attachment.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/attachments/:id` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-attachment/) |
| [Get Blog Post](actions/get-blog-post.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/blogposts/:id` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-blog-post/) |
| [Get Footer Comment](actions/get-footer-comment.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/footer-comments/:commentId` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-comment/) |
| [Get Page](actions/get-page.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/pages/:id` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-page/) |
| [Get Space](actions/get-space.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/spaces/:id` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-space/) |
| [Get Task](actions/get-task.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/tasks/:id` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-task/) |
| [List Accessible Resources](actions/list-accessible-resources.md) | `GET /oauth/token/accessible-resources` | [docs](https://developer.atlassian.com/cloud/confluence/oauth-2-3lo-apps/#siteaccess) |
| [List Attachments For Page](actions/list-attachments-for-page.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/pages/:id/attachments` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-page/) |
| [List Blog Posts](actions/list-blog-posts.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/blogposts` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-blog-post/) |
| [List Blog Posts In Space](actions/list-blog-posts-in-space.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/spaces/:id/blogposts` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-space/) |
| [List Footer Comments](actions/list-footer-comments.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/footer-comments` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-comment/) |
| [List Footer Comments For Page](actions/list-footer-comments-for-page.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/pages/:id/footer-comments` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-comment/) |
| [List Inline Comments For Page](actions/list-inline-comments-for-page.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/pages/:id/inline-comments` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-comment/) |
| [List Labels For Page](actions/list-labels-for-page.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/pages/:id/labels` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-page/) |
| [List Pages](actions/list-pages.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/pages` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-page/) |
| [List Pages In Space](actions/list-pages-in-space.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/spaces/:id/pages` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-space/) |
| [List Spaces](actions/list-spaces.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/spaces` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-space/) |
| [List Tasks](actions/list-tasks.md) | `GET /ex/confluence/:cloudId/wiki/api/v2/tasks` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-task/) |
| [Update Blog Post](actions/update-blog-post.md) | `PUT /ex/confluence/:cloudId/wiki/api/v2/blogposts/:id` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-blog-post/) |
| [Update Footer Comment](actions/update-footer-comment.md) | `PUT /ex/confluence/:cloudId/wiki/api/v2/footer-comments/:commentId` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-comment/) |
| [Update Page](actions/update-page.md) | `PUT /ex/confluence/:cloudId/wiki/api/v2/pages/:id` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-page/) |
| [Update Page Title](actions/update-page-title.md) | `PUT /ex/confluence/:cloudId/wiki/api/v2/pages/:id/title` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-page/) |
| [Update Task](actions/update-task.md) | `PUT /ex/confluence/:cloudId/wiki/api/v2/tasks/:id` | [docs](https://developer.atlassian.com/cloud/confluence/rest/v2/api-group-task/) |
