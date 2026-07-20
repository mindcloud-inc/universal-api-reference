# Testmo: Native API Reference

A consolidated summary of Testmo's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.testmo.com/api
- **OpenAPI specification:** https://docs.testmo.com/api/schema/openapi
- **API base URL:** `{apiBaseUrl}`

## Authentication

### API Key

Authenticate to a Testmo instance with a user API key sent as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required
- **API Base URL:** `apiBaseUrl` · required · Full Testmo instance API base URL ending in /api/v1, for example https://example.testmo.net/api/v1.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.testmo.com/api/introduction/api-authentication)

## API conventions

Responses from this API use JSON. The total page count is read from `last_page`. The current page number is read from `page`.

## Pagination

Use `per_page` in the query string to set the page size (default 100; accepted range 15–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Complete Automation Run](actions/complete-automation-run.md) | `POST /automation/runs/{automation_run_id}/complete` | [docs](https://support.testmo.com/hc/en-us/articles/37971158770957-Automation-Runs) |
| [Create Automation Run](actions/create-automation-run.md) | `POST /projects/{project_id}/automation/runs` | [docs](https://support.testmo.com/hc/en-us/articles/37971158770957-Automation-Runs) |
| [Get Automation Run](actions/get-automation-run.md) | `GET /automation/runs/{automation_run_id}` | [docs](https://support.testmo.com/hc/en-us/articles/37971158770957-Automation-Runs) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://docs.testmo.com/api/introduction/using-the-rest-api) |
| [Get Milestone](actions/get-milestone.md) | `GET /milestones/{milestone_id}` | [docs](https://support.testmo.com/hc/en-us/articles/38157425816717-Milestones) |
| [Get Project](actions/get-project.md) | `GET /projects/{project_id}` | [docs](https://support.testmo.com/hc/en-us/articles/38158978447885-Projects) |
| [Get Run](actions/get-run.md) | `GET /runs/{run_id}` | [docs](https://support.testmo.com/hc/en-us/articles/38159162797197-Runs) |
| [Get Session](actions/get-session.md) | `GET /sessions/{session_id}` | [docs](https://support.testmo.com/hc/en-us/articles/38159977518989-Sessions) |
| [Get User](actions/get-user.md) | `GET /users/{user_id}` | [docs](https://support.testmo.com/hc/en-us/articles/38165363497741-Users) |
| [List Automation Runs](actions/list-automation-runs.md) | `GET /projects/{project_id}/automation/runs` | [docs](https://support.testmo.com/hc/en-us/articles/37971158770957-Automation-Runs) |
| [List Automation Sources](actions/list-automation-sources.md) | `GET /projects/{project_id}/automation/sources` | [docs](https://support.testmo.com/hc/en-us/articles/37974874224141-Automation-Sources) |
| [List Case Attachments](actions/list-case-attachments.md) | `GET /cases/{case_id}/attachments` | [docs](https://support.testmo.com/hc/en-us/articles/40045804558093-Attachments) |
| [List Cases](actions/list-cases.md) | `GET /projects/{project_id}/cases` | [docs](https://support.testmo.com/hc/en-us/articles/40051160964749-Cases) |
| [List Folders](actions/list-folders.md) | `GET /projects/{project_id}/folders` | [docs](https://support.testmo.com/hc/en-us/articles/40067196221837-Folders) |
| [List Milestones](actions/list-milestones.md) | `GET /projects/{project_id}/milestones` | [docs](https://support.testmo.com/hc/en-us/articles/38157425816717-Milestones) |
| [List Project Users](actions/list-project-users.md) | `GET /projects/{project_id}/users` | [docs](https://support.testmo.com/hc/en-us/articles/38165363497741-Users) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://support.testmo.com/hc/en-us/articles/38158978447885-Projects) |
| [List Runs](actions/list-runs.md) | `GET /projects/{project_id}/runs` | [docs](https://support.testmo.com/hc/en-us/articles/38159162797197-Runs) |
| [List Sessions](actions/list-sessions.md) | `GET /projects/{project_id}/sessions` | [docs](https://support.testmo.com/hc/en-us/articles/38159977518989-Sessions) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://support.testmo.com/hc/en-us/articles/38165363497741-Users) |
