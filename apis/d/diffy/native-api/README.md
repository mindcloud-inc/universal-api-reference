# Diffy: Native API Reference

A consolidated summary of Diffy's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://app.diffy.website/rest
- **OpenAPI specification:** https://app.diffy.website/rest/swagger.json
- **API base URL:** `https://app.diffy.website/api`

## Authentication

### API Key Login

Exchange a Diffy API key for a bearer token before API requests.

### Credentials

- **API Key:** `apiKey` · required · Diffy API key used to exchange for a bearer token.

Send these headers with each API request:

```http
Authorization: Bearer <custom.token>
```

[Official authentication documentation](https://github.com/DiffyWebsite/diffy-cli)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `projects`. The total page count is read from `totalPages`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compare Environments](actions/compare-environments.md) | `POST /projects/:id/compare` | [docs](https://app.diffy.website/rest) |
| [Create Custom Uploaded Screenshot](actions/create-custom-uploaded-screenshot.md) | `POST /projects/:id/create-custom-snapshot` | [docs](https://app.diffy.website/rest) |
| [Create Diff](actions/create-diff.md) | `POST /projects/:id/diffs` | [docs](https://app.diffy.website/rest) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://app.diffy.website/rest) |
| [Create Screenshot](actions/create-screenshot.md) | `POST /projects/:id/screenshots` | [docs](https://app.diffy.website/rest) |
| [Delete Diff](actions/delete-diff.md) | `DELETE /diffs/:id` | [docs](https://app.diffy.website/rest) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://app.diffy.website/rest) |
| [Delete Screenshot](actions/delete-screenshot.md) | `DELETE /snapshots/:id` | [docs](https://app.diffy.website/rest) |
| [Exchange API Key for Token](actions/exchange-api-key-for-token.md) | `POST /auth/key` | [docs](https://app.diffy.website/rest) |
| [Get Diff](actions/get-diff.md) | `GET /diffs/:id` | [docs](https://app.diffy.website/rest) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://app.diffy.website/rest) |
| [Get Screenshot](actions/get-screenshot.md) | `GET /snapshots/:id` | [docs](https://app.diffy.website/rest) |
| [List Project Diffs](actions/list-project-diffs.md) | `GET /projects/:id/diffs` | [docs](https://app.diffy.website/rest) |
| [List Project Screenshots](actions/list-project-screenshots.md) | `GET /projects/:id/screenshots` | [docs](https://app.diffy.website/rest) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://app.diffy.website/rest) |
| [Set Baseline Image](actions/set-baseline-image.md) | `PUT /projects/:id/set-base-line-image/:screenshot_id` | [docs](https://app.diffy.website/rest) |
| [Set Screenshot Set as Baseline](actions/set-screenshot-set-as-baseline.md) | `PUT /projects/:id/set-base-line-set/:screenshot_id` | [docs](https://app.diffy.website/rest) |
| [Start or Stop Diff Jobs](actions/start-or-stop-diff-jobs.md) | `PUT /diffs/:id/:action` | [docs](https://app.diffy.website/rest) |
| [Start or Stop Screenshot Jobs](actions/start-or-stop-screenshot-jobs.md) | `PUT /snapshots/:id/:action` | [docs](https://app.diffy.website/rest) |
| [Update Diff Name](actions/update-diff-name.md) | `PUT /diffs/:id` | [docs](https://app.diffy.website/rest) |
| [Update Project](actions/update-project.md) | `POST /projects/:id` | [docs](https://app.diffy.website/rest) |
| [Update Screenshot](actions/update-screenshot.md) | `PUT /snapshots/:id` | [docs](https://app.diffy.website/rest) |
