# Crowdin: Native API Reference

A consolidated summary of Crowdin's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://support.crowdin.com/developer/api/v2/
- **OpenAPI specification:** https://support.crowdin.com/src/assets/api/crowdin/file-based.yml
- **API base URL:** `https://api.crowdin.com/api/v2`

## Authentication

### Personal Access Token

Use a Crowdin Personal Access Token in the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.crowdin.com/account-settings/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–500). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `orderBy` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Branch](actions/add-branch.md) | `POST /projects/:projectId/branches` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.branches.post) |
| [Add Directory](actions/add-directory.md) | `POST /projects/:projectId/directories` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.directories.post) |
| [Add File](actions/add-file.md) | `POST /projects/:projectId/files` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.files.post) |
| [Add Project](actions/add-project.md) | `POST /projects` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.post) |
| [Add Project Task](actions/add-project-task.md) | `POST /projects/:projectId/tasks` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.tasks.post) |
| [Add Storage](actions/add-storage.md) | `POST /storages` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.storages.post) |
| [Build Project Translation](actions/build-project-translation.md) | `POST /projects/:projectId/translations/builds` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.translations.builds.post) |
| [Download File](actions/download-file.md) | `GET /projects/:projectId/files/:fileId/download` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.files.download.get) |
| [Download Project Translations](actions/download-project-translations.md) | `GET /projects/:projectId/translations/builds/:buildId/download` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.translations.builds.download.download) |
| [Edit File](actions/edit-file.md) | `PATCH /projects/:projectId/files/:fileId` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.files.patch) |
| [Edit Project](actions/edit-project.md) | `PATCH /projects/:projectId` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.patch) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /user` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.user.get) |
| [Get File](actions/get-file.md) | `GET /projects/:projectId/files/:fileId` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.files.get) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.get) |
| [Get Project Build Status](actions/get-project-build-status.md) | `GET /projects/:projectId/translations/builds/:buildId` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.translations.builds.get) |
| [Get Project Progress](actions/get-project-progress.md) | `GET /projects/:projectId/languages/progress` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.languages.progress.getMany) |
| [Get Project Task](actions/get-project-task.md) | `GET /projects/:projectId/tasks/:taskId` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.tasks.get) |
| [List Branches](actions/list-branches.md) | `GET /projects/:projectId/branches` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.branches.getMany) |
| [List Directories](actions/list-directories.md) | `GET /projects/:projectId/directories` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.directories.getMany) |
| [List File Revisions](actions/list-file-revisions.md) | `GET /projects/:projectId/files/:fileId/revisions` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.files.revisions.getMany) |
| [List Files](actions/list-files.md) | `GET /projects/:projectId/files` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.files.getMany) |
| [List Project Builds](actions/list-project-builds.md) | `GET /projects/:projectId/translations/builds` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.translations.builds.getMany) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /projects/:projectId/tasks` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.tasks.getMany) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.projects.getMany) |
| [List Supported Languages](actions/list-supported-languages.md) | `GET /languages` | [docs](https://support.crowdin.com/developer/api/v2/#operation/api.languages.getMany) |
