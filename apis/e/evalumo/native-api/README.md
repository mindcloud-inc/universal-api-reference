# Evalumo: Native API Reference

A consolidated summary of Evalumo's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://evalumo.apidocumentation.com/reference
- **API base URL:** `https://api.evalumo.com`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.evalumo.com/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.evalumo.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.evalumo.com/refreshToken.

[Official authentication documentation](https://evalumo.apidocumentation.com/guide)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | `POST /project` | [docs](https://evalumo.apidocumentation.com/reference#tag/project/POST/project) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://evalumo.apidocumentation.com/reference#tag/user/GET/user) |
| [Get Exported Project](actions/get-exported-project.md) | `GET /exportedProject/:lookup` | [docs](https://evalumo.apidocumentation.com/reference#tag/exported-project/GET/exportedProject/{idOrName}) |
| [List Exported Projects](actions/list-exported-projects.md) | `GET /exportedProject` | [docs](https://evalumo.apidocumentation.com/reference#tag/exported-project/GET/exportedProject) |
| [List Projects](actions/list-projects.md) | `GET /project` | [docs](https://evalumo.apidocumentation.com/guide/getting-started) |
| [Subscribe To Export Webhook](actions/subscribe-to-export-webhook.md) | `POST /hook` | [docs](https://evalumo.apidocumentation.com/reference#tag/webhooks/POST/hook) |
| [Update Project](actions/update-project.md) | `PATCH /project/:projectId` | [docs](https://evalumo.apidocumentation.com/reference#tag/project/PATCH/project/{projectId}) |
| [Update Project Category](actions/update-project-category.md) | `PATCH /project/:projectId` | [docs](https://evalumo.apidocumentation.com/reference#tag/project/PATCH/project/{projectId}) |
