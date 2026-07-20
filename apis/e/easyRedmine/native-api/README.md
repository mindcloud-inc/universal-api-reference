# Easy Redmine: Native API Reference

A consolidated summary of Easy Redmine's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.easy8.com/documentation-of-easy8/article/rest-api-specification
- **OpenAPI specification:** https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml
- **API base URL:** `https://3f73561b8b.bigus-e5.easy8.com`

## Authentication

### API Key

Authenticate with an Easy Redmine API access key sent in the X-Redmine-API-Key request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.easy8.com/services/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `total_count`. The current page number is read from `offset`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Issue To Favorites](actions/add-issue-to-favorites.md) | `POST /easy_issues/:id/favorite.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Add Issue Watcher](actions/add-issue-watcher.md) | `POST /issues/:id/watchers.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Add Project To Favorites](actions/add-project-to-favorites.md) | `POST /projects/:id/favorite.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Add User To Group](actions/add-user-to-group.md) | `POST /groups/:id/users.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Archive Project](actions/archive-project.md) | `POST /projects/:id/archive.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Close Project](actions/close-project.md) | `POST /projects/:id/close.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Create Group](actions/create-group.md) | `POST /groups.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Create Issue](actions/create-issue.md) | `POST /issues.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Create Project](actions/create-project.md) | `POST /projects.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /time_entries.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Create Version](actions/create-version.md) | `POST /projects/:projectId/versions.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Delete Issue](actions/delete-issue.md) | `DELETE /issues/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Delete Time Entry](actions/delete-time-entry.md) | `DELETE /time_entries/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Delete Version](actions/delete-version.md) | `DELETE /versions/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Get Custom Field](actions/get-custom-field.md) | `GET /custom_fields/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Get Group](actions/get-group.md) | `GET /groups/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Get Issue](actions/get-issue.md) | `GET /issues/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Get Project](actions/get-project.md) | `GET /projects/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /time_entries/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Get Version](actions/get-version.md) | `GET /versions/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom_fields.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [List Groups](actions/list-groups.md) | `GET /groups.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [List Issues](actions/list-issues.md) | `GET /issues.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [List Projects](actions/list-projects.md) | `GET /projects.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [List Time Entries](actions/list-time-entries.md) | `GET /time_entries.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [List Versions](actions/list-versions.md) | `GET /versions.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Remove Issue From Favorites](actions/remove-issue-from-favorites.md) | `POST /easy_issues/:id/unfavorite.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Remove Issue Watcher](actions/remove-issue-watcher.md) | `DELETE /issues/:id/watchers/:userId.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Remove Project From Favorites](actions/remove-project-from-favorites.md) | `POST /projects/:id/unfavorite.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Remove User From Group](actions/remove-user-from-group.md) | `DELETE /groups/:id/users/:userId.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Reopen Project](actions/reopen-project.md) | `POST /projects/:id/reopen.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Search](actions/search.md) | `GET /search.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Unarchive Project](actions/unarchive-project.md) | `POST /projects/:id/unarchive.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Update Group](actions/update-group.md) | `PUT /groups/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Update Issue](actions/update-issue.md) | `PUT /issues/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Update Time Entry](actions/update-time-entry.md) | `PUT /time_entries/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
| [Update Version](actions/update-version.md) | `PUT /versions/:id.json` | [docs](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml) |
