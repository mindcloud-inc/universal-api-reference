# ParseHub: Native API Reference

A consolidated summary of ParseHub's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://www.parsehub.com/docs/ref/api/v2/
- **API base URL:** `https://www.parsehub.com/api/v2`

## Authentication

### API Key

Use your ParseHub API key. ParseHub requires the key as the documented api_key request parameter rather than a bearer header.

### Credentials

- **API Key:** `apiKey` · required · Your ParseHub account API key from the ParseHub account page. This value is sent as the ParseHub `api_key` request parameter.

[Official authentication documentation](https://help.parsehub.com/hc/en-us/articles/223858607-Connect-to-the-ParseHub-API)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded; charset=utf-8` |

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Run](actions/cancel-run.md) | `POST /runs/{run_token}/cancel` | [docs](https://www.parsehub.com/docs/ref/api/v2/#cancel-a-run) |
| [Delete Run](actions/delete-run.md) | `DELETE /runs/{run_token}` | [docs](https://www.parsehub.com/docs/ref/api/v2/#delete-a-run) |
| [Get Last Ready Data (CSV)](actions/get-last-ready-data-csv.md) | `GET /projects/{project_token}/last_ready_run/data` | [docs](https://www.parsehub.com/docs/ref/api/v2/#get-last-ready-data) |
| [Get Last Ready Data (JSON)](actions/get-last-ready-data-json.md) | `GET /projects/{project_token}/last_ready_run/data` | [docs](https://www.parsehub.com/docs/ref/api/v2/#get-last-ready-data) |
| [Get Project](actions/get-project.md) | `GET /projects/{project_token}` | [docs](https://www.parsehub.com/docs/ref/api/v2/#get-a-project) |
| [Get Run](actions/get-run.md) | `GET /runs/{run_token}` | [docs](https://www.parsehub.com/docs/ref/api/v2/#get-a-run) |
| [Get Run Data (CSV)](actions/get-run-data-csv.md) | `GET /runs/{run_token}/data` | [docs](https://www.parsehub.com/docs/ref/api/v2/#get-data-for-a-run) |
| [Get Run Data (JSON)](actions/get-run-data-json.md) | `GET /runs/{run_token}/data` | [docs](https://www.parsehub.com/docs/ref/api/v2/#get-data-for-a-run) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://www.parsehub.com/docs/ref/api/v2/#list-all-projects) |
| [Run Project](actions/run-project.md) | `POST /projects/{project_token}/run` | [docs](https://www.parsehub.com/docs/ref/api/v2/#run-a-project) |
