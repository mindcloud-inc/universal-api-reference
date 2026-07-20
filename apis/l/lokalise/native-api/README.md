# Lokalise: Native API Reference

A consolidated summary of Lokalise's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://developers.lokalise.com/reference/lokalise-rest-api
- **API base URL:** `https://api.lokalise.com/api2`

## Authentication

### API Key

Use a Lokalise API token sent in the X-Api-Token header.

### Credentials

- **API Key:** `apiKey` · required · Your Lokalise API token.

Send these headers with each API request:

```http
X-Api-Token: <apiKey>
```

[Official authentication documentation](https://developers.lokalise.com/reference/api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `projects`.

## Pagination

Use `limit` in the query string to set the page size (default 100; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Comments](actions/create-comments.md) | `POST /projects/:project_id/keys/:key_id/comments` | [docs](https://developers.lokalise.com/reference/create-comments) |
| [Create Contributors](actions/create-contributors.md) | `POST /projects/:project_id/contributors` | [docs](https://developers.lokalise.com/reference/create-contributors) |
| [Create Keys](actions/create-keys.md) | `POST /projects/:project_id/keys` | [docs](https://developers.lokalise.com/reference/create-keys) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://developers.lokalise.com/reference/create-a-project) |
| [Create Screenshots](actions/create-screenshots.md) | `POST /projects/:project_id/screenshots` | [docs](https://developers.lokalise.com/reference/create-screenshots) |
| [Create Snapshot](actions/create-snapshot.md) | `POST /projects/:project_id/snapshots` | [docs](https://developers.lokalise.com/reference/create-a-snapshot) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /projects/:project_id/keys/:key_id/comments/:comment_id` | [docs](https://developers.lokalise.com/reference/delete-a-comment) |
| [Delete Contributor](actions/delete-contributor.md) | `DELETE /projects/:project_id/contributors/:contributor_id` | [docs](https://developers.lokalise.com/reference/delete-a-contributor) |
| [Delete Key](actions/delete-key.md) | `DELETE /projects/:project_id/keys/:key_id` | [docs](https://developers.lokalise.com/reference/delete-a-key) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:project_id` | [docs](https://developers.lokalise.com/reference/delete-a-project) |
| [Delete Screenshot](actions/delete-screenshot.md) | `DELETE /projects/:project_id/screenshots/:screenshot_id` | [docs](https://developers.lokalise.com/reference/delete-a-screenshot) |
| [Delete Snapshot](actions/delete-snapshot.md) | `DELETE /projects/:project_id/snapshots/:snapshot_id` | [docs](https://developers.lokalise.com/reference/delete-a-snapshot) |
| [Download Files Async](actions/download-files-async.md) | `POST /projects/:project_id/files/async-download` | [docs](https://developers.lokalise.com/reference/download-files-async) |
| [List Branches](actions/list-branches.md) | `GET /projects/:project_id/branches` | [docs](https://developers.lokalise.com/reference/list-all-branches) |
| [List Contributors](actions/list-contributors.md) | `GET /projects/:project_id/contributors` | [docs](https://developers.lokalise.com/reference/list-all-contributors) |
| [List Key Comments](actions/list-key-comments.md) | `GET /projects/:project_id/keys/:key_id/comments` | [docs](https://developers.lokalise.com/reference/list-key-comments) |
| [List Keys](actions/list-keys.md) | `GET /projects/:project_id/keys` | [docs](https://developers.lokalise.com/reference/list-all-keys) |
| [List Processes](actions/list-processes.md) | `GET /projects/:project_id/processes` | [docs](https://developers.lokalise.com/reference/list-all-processes) |
| [List Project Languages](actions/list-project-languages.md) | `GET /projects/:project_id/languages` | [docs](https://developers.lokalise.com/reference/list-project-languages) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developers.lokalise.com/reference/list-all-projects) |
| [List Screenshots](actions/list-screenshots.md) | `GET /projects/:project_id/screenshots` | [docs](https://developers.lokalise.com/reference/list-all-screenshots) |
| [List Snapshots](actions/list-snapshots.md) | `GET /projects/:project_id/snapshots` | [docs](https://developers.lokalise.com/reference/list-all-snapshots) |
| [List Tasks](actions/list-tasks.md) | `GET /projects/:project_id/tasks` | [docs](https://developers.lokalise.com/reference/list-all-tasks) |
| [List Translations](actions/list-translations.md) | `GET /projects/:project_id/translations` | [docs](https://developers.lokalise.com/reference/list-all-translations) |
| [Restore Snapshot](actions/restore-snapshot.md) | `POST /projects/:project_id/snapshots/:snapshot_id` | [docs](https://developers.lokalise.com/reference/restore-a-snapshot) |
| [Retrieve Key](actions/retrieve-key.md) | `GET /projects/:project_id/keys/:key_id` | [docs](https://developers.lokalise.com/reference/retrieve-a-key) |
| [Retrieve Process](actions/retrieve-process.md) | `GET /projects/:project_id/processes/:process_id` | [docs](https://developers.lokalise.com/reference/retrieve-a-process) |
| [Retrieve Project](actions/retrieve-project.md) | `GET /projects/:project_id` | [docs](https://developers.lokalise.com/reference/retrieve-a-project) |
| [Retrieve Screenshot](actions/retrieve-screenshot.md) | `GET /projects/:project_id/screenshots/:screenshot_id` | [docs](https://developers.lokalise.com/reference/retrieve-a-screenshot) |
| [Update Contributor](actions/update-contributor.md) | `PUT /projects/:project_id/contributors/:contributor_id` | [docs](https://developers.lokalise.com/reference/update-a-contributor) |
| [Update Key](actions/update-key.md) | `PUT /projects/:project_id/keys/:key_id` | [docs](https://developers.lokalise.com/reference/update-a-key) |
| [Update Project](actions/update-project.md) | `PUT /projects/:project_id` | [docs](https://developers.lokalise.com/reference/update-a-project) |
