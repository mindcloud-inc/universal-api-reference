# Hyperbrowser: Native API Reference

A consolidated summary of Hyperbrowser's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.hyperbrowser.ai/docs/introduction
- **API base URL:** `https://api.hyperbrowser.ai`

## Authentication

### API Key

Use a Hyperbrowser API key from the Hyperbrowser Dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.hyperbrowser.ai/docs/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Profile](actions/create-profile.md) | `POST /api/profile` | [docs](https://www.hyperbrowser.ai/docs/api-reference/creates-a-new-profile) |
| [Create Scrape Job](actions/create-scrape-job.md) | `POST /api/scrape` | [docs](https://www.hyperbrowser.ai/docs/api-reference/create-new-scrape-job) |
| [Create Session](actions/create-session.md) | `POST /api/session` | [docs](https://www.hyperbrowser.ai/docs/api-reference/create-new-session) |
| [Delete Profile](actions/delete-profile.md) | `DELETE /api/profile/:id` | [docs](https://www.hyperbrowser.ai/docs/api-reference/delete-profile-by-id) |
| [Fetch Web Page](actions/fetch-web-page.md) | `POST /api/web/fetch` | [docs](https://www.hyperbrowser.ai/docs/api-reference/fetch-a-web-page) |
| [Get Browser Use Task Status and Results](actions/get-browser-use-task-status-and-results.md) | `GET /api/task/browser-use/:id` | [docs](https://www.hyperbrowser.ai/docs/api-reference/get-browser-use-task-status-and-results) |
| [Get Crawl Job Status and Results](actions/get-crawl-job-status-and-results.md) | `GET /api/crawl/:id` | [docs](https://www.hyperbrowser.ai/docs/api-reference/get-crawl-job-status-and-results) |
| [Get Extract Job Status and Results](actions/get-extract-job-status-and-results.md) | `GET /api/extract/:id` | [docs](https://www.hyperbrowser.ai/docs/api-reference/get-extract-job-status-and-results) |
| [Get HyperAgent Task Status and Results](actions/get-hyperagent-task-status-and-results.md) | `GET /api/task/hyper-agent/:id` | [docs](https://www.hyperbrowser.ai/docs/api-reference/get-hyperagent-task-status-and-results) |
| [Get Profile](actions/get-profile.md) | `GET /api/profile/:id` | [docs](https://www.hyperbrowser.ai/docs/api-reference/get-profile-by-id) |
| [Get Scrape Job Status and Result](actions/get-scrape-job-status-and-result.md) | `GET /api/scrape/:id` | [docs](https://www.hyperbrowser.ai/docs/api-reference/get-scrape-job-status-and-result) |
| [Get Session](actions/get-session.md) | `GET /api/session/:id` | [docs](https://www.hyperbrowser.ai/docs/api-reference/get-session-by-id) |
| [Get Web Crawl Job Results](actions/get-web-crawl-job-results.md) | `GET /api/web/crawl/:id` | [docs](https://www.hyperbrowser.ai/docs/api-reference/get-web-crawl-job-results) |
| [List Profiles](actions/list-profiles.md) | `GET /api/profiles` | [docs](https://www.hyperbrowser.ai/docs/api-reference/get-list-of-profiles) |
| [List Sessions](actions/list-sessions.md) | `GET /api/sessions` | [docs](https://www.hyperbrowser.ai/docs/api-reference/get-list-of-sessions) |
| [Search the Web](actions/search-the-web.md) | `POST /api/web/search` | [docs](https://www.hyperbrowser.ai/docs/api-reference/search-the-web) |
| [Start Browser Use Task](actions/start-browser-use-task.md) | `POST /api/task/browser-use` | [docs](https://www.hyperbrowser.ai/docs/api-reference/start-a-browser-use-task) |
| [Start Crawl Job](actions/start-crawl-job.md) | `POST /api/crawl` | [docs](https://www.hyperbrowser.ai/docs/api-reference/start-a-crawl-job) |
| [Start Extract Job](actions/start-extract-job.md) | `POST /api/extract` | [docs](https://www.hyperbrowser.ai/docs/api-reference/start-an-extract-job) |
| [Start HyperAgent Task](actions/start-hyperagent-task.md) | `POST /api/task/hyper-agent` | [docs](https://www.hyperbrowser.ai/docs/api-reference/start-a-hyperagent-task) |
| [Start Web Crawl Job](actions/start-web-crawl-job.md) | `POST /api/web/crawl` | [docs](https://www.hyperbrowser.ai/docs/api-reference/start-a-web-crawl-job) |
| [Stop Browser Use Task](actions/stop-browser-use-task.md) | `PUT /api/task/browser-use/:id/stop` | [docs](https://www.hyperbrowser.ai/docs/api-reference/stop-a-browser-use-task) |
| [Stop HyperAgent Task](actions/stop-hyperagent-task.md) | `PUT /api/task/hyper-agent/:id/stop` | [docs](https://www.hyperbrowser.ai/docs/api-reference/stop-a-hyperagent-task) |
| [Stop Session](actions/stop-session.md) | `PUT /api/session/:id/stop` | [docs](https://www.hyperbrowser.ai/docs/api-reference/stop-a-session) |
