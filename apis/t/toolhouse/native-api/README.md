# Toolhouse: Native API Reference

A consolidated summary of Toolhouse's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.toolhouse.ai/toolhouse/agent-workers
- **API base URL:** `https://api.toolhouse.ai/v1`

## Authentication

### API Key

Use your Toolhouse API key to authenticate requests to the Toolhouse API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.toolhouse.ai/toolhouse/run-agents-as-apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Continue Agent Run](actions/continue-agent-run.md) | `PUT /agent-runs/:run_id` | [docs](https://docs.toolhouse.ai/toolhouse/agent-workers/running-agents-asynchronously/api-reference) |
| [Convert Text to Cron](actions/convert-text-to-cron.md) | `GET /schedules/text-to-cron` | [docs](https://docs.toolhouse.ai/toolhouse/agent-workers/schedule-autonomous-runs/api-reference) |
| [Create Agent Run](actions/create-agent-run.md) | `POST /agent-runs` | [docs](https://docs.toolhouse.ai/toolhouse/agent-workers/running-agents-asynchronously/api-reference) |
| [Create Schedule](actions/create-schedule.md) | `POST /schedules` | [docs](https://docs.toolhouse.ai/toolhouse/agent-workers/schedule-autonomous-runs/api-reference) |
| [Delete Schedule](actions/delete-schedule.md) | `DELETE /schedules/:schedule_id` | [docs](https://docs.toolhouse.ai/toolhouse/agent-workers/schedule-autonomous-runs/api-reference) |
| [Get Agent Run](actions/get-agent-run.md) | `GET /agent-runs/:run_id` | [docs](https://docs.toolhouse.ai/toolhouse/agent-workers/running-agents-asynchronously/api-reference) |
| [Get Schedule](actions/get-schedule.md) | `GET /schedules/:schedule_id` | [docs](https://docs.toolhouse.ai/toolhouse/agent-workers/schedule-autonomous-runs/api-reference) |
| [List Agent Runs](actions/list-agent-runs.md) | `GET /agent-runs` | [docs](https://docs.toolhouse.ai/toolhouse/agent-workers/running-agents-asynchronously/api-reference) |
| [List Schedules](actions/list-schedules.md) | `GET /schedules` | [docs](https://docs.toolhouse.ai/toolhouse/agent-workers/schedule-autonomous-runs/api-reference) |
| [Update Schedule](actions/update-schedule.md) | `PUT /schedules/:schedule_id` | [docs](https://docs.toolhouse.ai/toolhouse/agent-workers/schedule-autonomous-runs/api-reference) |
