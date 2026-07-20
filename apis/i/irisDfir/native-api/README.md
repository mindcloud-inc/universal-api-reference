# Iris Dfir: Native API Reference

A consolidated summary of Iris Dfir's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://docs.dfir-iris.org/latest/operations/api/
- **API base URL:** `https://v200.beta.dfir-iris.org`

## Authentication

### API Key

Connect Iris Dfir using the API key from My settings in the IRIS web app.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.dfir-iris.org/latest/operations/api/)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | query | `number` | yes | IRIS access-control context identifier required on every API request. |

Responses from this API use JSON. The total page count is read from `last_page`. The current page number is read from `current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–250). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `sort_dir`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Note](actions/add-note.md) | `POST /case/notes/add` | [docs](https://docs.dfir-iris.org/2.4.20/_static/iris_api_reference_v2.0.4.html#tag/Case-notes/operation/case_notes_add_post) |
| [Create Asset](actions/create-asset.md) | `POST /api/v2/cases/:case_identifier/assets` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Assets/operation/api_v2_cases_(case_identifier)_assets_post) |
| [Create Case](actions/create-case.md) | `POST /api/v2/cases` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Cases/operation/api_v2_cases_post) |
| [Create Task](actions/create-task.md) | `POST /api/v2/cases/:case_identifier/tasks` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Tasks/operation/api_v2_cases_(case_identifier)_tasks_post) |
| [Delete Asset](actions/delete-asset.md) | `DELETE /api/v2/cases/:case_identifier/assets/:identifier` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Assets/operation/api_v2_cases_(case_identifier)_assets_(identifier)_delete) |
| [Delete Case](actions/delete-case.md) | `DELETE /api/v2/cases/:case_identifier` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Cases/operation/api_v2_cases_(case_identifier)_delete) |
| [Delete Note](actions/delete-note.md) | `POST /case/notes/delete/:identifier` | [docs](https://docs.dfir-iris.org/2.4.20/_static/iris_api_reference_v2.0.4.html#tag/Case-notes/operation/case_notes_delete_(note_id)_post) |
| [Delete Task](actions/delete-task.md) | `DELETE /api/v2/cases/:case_identifier/tasks/:identifier` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Tasks/operation/api_v2_cases_(case_identifier)_tasks_(identifier)_delete) |
| [Get Asset](actions/get-asset.md) | `GET /api/v2/cases/:case_identifier/assets/:identifier` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Assets/operation/api_v2_cases_(case_identifier)_assets_(identifier)_get) |
| [Get Case](actions/get-case.md) | `GET /api/v2/cases/:case_identifier` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Cases/operation/api_v2_cases_(case_identifier)_get) |
| [Get Note](actions/get-note.md) | `GET /case/notes/:identifier` | [docs](https://docs.dfir-iris.org/2.4.20/_static/iris_api_reference_v2.0.4.html#tag/Case-notes/operation/case_notes_(note_id)_get) |
| [Get Task](actions/get-task.md) | `GET /api/v2/cases/:case_identifier/tasks/:identifier` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Tasks/operation/api_v2_cases_(case_identifier)_tasks_(identifier)_get) |
| [List Alerts](actions/list-alerts.md) | `GET /api/v2/alerts` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Alerts) |
| [List Alerts Legacy](actions/list-alerts-legacy.md) | `GET /alerts/filter` | [docs](https://docs.dfir-iris.org/2.4.20/_static/iris_api_reference_v2.0.4.html#tag/Alerts/operation/alerts_filter_get) |
| [List Assets](actions/list-assets.md) | `GET /api/v2/cases/:case_identifier/assets` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Assets/operation/api_v2_cases_(case_identifier)_assets_get) |
| [List Cases](actions/list-cases.md) | `GET /api/v2/cases` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Cases/operation/api_v2_cases_get) |
| [List Note Directories](actions/list-note-directories.md) | `GET /case/notes/directories/filter` | [docs](https://docs.dfir-iris.org/2.4.20/_static/iris_api_reference_v2.0.4.html#tag/Case-notes/operation/case_notes_directories_filter_get) |
| [List Tasks](actions/list-tasks.md) | `GET /api/v2/cases/:case_identifier/tasks` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Tasks/operation/api_v2_cases_(case_identifier)_tasks_get) |
| [Update Asset](actions/update-asset.md) | `PUT /api/v2/cases/:case_identifier/assets/:identifier` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Assets/operation/api_v2_cases_(case_identifier)_assets_(identifier)_put) |
| [Update Case](actions/update-case.md) | `PUT /api/v2/cases/:case_identifier` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Cases/operation/api_v2_cases_(case_identifier)_put) |
| [Update Note](actions/update-note.md) | `POST /case/notes/update/:identifier` | [docs](https://docs.dfir-iris.org/2.4.20/_static/iris_api_reference_v2.0.4.html#tag/Case-notes/operation/case_notes_update_(note_id)_post) |
| [Update Task](actions/update-task.md) | `PUT /api/v2/cases/:case_identifier/tasks/:identifier` | [docs](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Tasks/operation/api_v2_cases_(case_identifier)_tasks_(identifier)_put) |
