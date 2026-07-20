# Dribbble: Native API Reference

A consolidated summary of Dribbble's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://developer.dribbble.com/v2/
- **API base URL:** `https://api.dribbble.com/v2`

## Authentication

### OAuth2

Connect a Dribbble account with OAuth2 authorization code.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://dribbble.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://dribbble.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `public upload`.

[Official authentication documentation](https://developer.dribbble.com/v2/oauth/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 30; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1. Follow the complete next-page URL returned by the API.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | `POST /jobs` | [docs](https://developer.dribbble.com/v2/jobs/) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://developer.dribbble.com/v2/projects/) |
| [Create Shot](actions/create-shot.md) | `POST /shots` | [docs](https://developer.dribbble.com/v2/shots/) |
| [Create Shot Attachment](actions/create-shot-attachment.md) | `POST /shots/:shot/attachments` | [docs](https://developer.dribbble.com/v2/attachments/) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://developer.dribbble.com/v2/projects/) |
| [Delete Shot](actions/delete-shot.md) | `DELETE /shots/:id` | [docs](https://developer.dribbble.com/v2/shots/) |
| [Delete Shot Attachment](actions/delete-shot-attachment.md) | `DELETE /shots/:shot/attachments/:id` | [docs](https://developer.dribbble.com/v2/attachments/) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://developer.dribbble.com/v2/user/) |
| [Get Job](actions/get-job.md) | `GET /jobs/:id` | [docs](https://developer.dribbble.com/v2/jobs/) |
| [Get Shot](actions/get-shot.md) | `GET /shots/:id` | [docs](https://developer.dribbble.com/v2/shots/) |
| [List User Projects](actions/list-user-projects.md) | `GET /user/projects` | [docs](https://developer.dribbble.com/v2/projects/) |
| [List User Shots](actions/list-user-shots.md) | `GET /user/shots` | [docs](https://developer.dribbble.com/v2/shots/) |
| [Update Job](actions/update-job.md) | `PUT /jobs/:id` | [docs](https://developer.dribbble.com/v2/jobs/) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://developer.dribbble.com/v2/projects/) |
| [Update Shot](actions/update-shot.md) | `PUT /shots/:id` | [docs](https://developer.dribbble.com/v2/shots/) |
