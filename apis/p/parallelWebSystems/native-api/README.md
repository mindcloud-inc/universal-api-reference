# Parallel Web Systems: Native API Reference

A consolidated summary of Parallel Web Systems's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://docs.parallel.ai/getting-started/overview
- **OpenAPI specification:** https://docs.parallel.ai/public-openapi.json
- **API base URL:** `https://api.parallel.ai`

## Authentication

### API Key

Use a Parallel API key. MindCloud injects the stored secret as the x-api-key header on every request.

### Credentials

- **API Key:** `apiKey` · required · Paste the Parallel API key value from Settings > API Keys. MindCloud sends it as the x-api-key header.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.parallel.ai/getting-started/overview)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Enrichment to FindAll Run](actions/add-enrichment-to-find-all-run.md) | `POST /v1beta/findall/runs/:findall_id/enrich` | [docs](https://docs.parallel.ai/api-reference/findall-api-beta/add-enrichment-to-findall-run) |
| [Add Runs to Task Group](actions/add-runs-to-task-group.md) | `POST /v1beta/tasks/groups/:taskgroup_id/runs` | [docs](https://docs.parallel.ai/api-reference/task-groups-beta/add-runs-to-task-group) |
| [Cancel FindAll Run](actions/cancel-find-all-run.md) | `POST /v1beta/findall/runs/:findall_id/cancel` | [docs](https://docs.parallel.ai/api-reference/findall-api-beta/cancel-findall-run) |
| [Chat Completions](actions/chat-completions.md) | `POST /v1beta/chat/completions` | [docs](https://docs.parallel.ai/api-reference/chat-api-beta/chat-completions) |
| [Create FindAll Run](actions/create-find-all-run.md) | `POST /v1beta/findall/runs` | [docs](https://docs.parallel.ai/api-reference/findall-api-beta/create-findall-run) |
| [Create Monitor](actions/create-monitor.md) | `POST /v1alpha/monitors` | [docs](https://docs.parallel.ai/api-reference/monitor/create-monitor) |
| [Create Task Group](actions/create-task-group.md) | `POST /v1beta/tasks/groups` | [docs](https://docs.parallel.ai/api-reference/task-groups-beta/create-task-group) |
| [Create Task Run](actions/create-task-run.md) | `POST /v1/tasks/runs` | [docs](https://docs.parallel.ai/api-reference/tasks-v1/create-task-run) |
| [Delete Monitor](actions/delete-monitor.md) | `DELETE /v1alpha/monitors/:monitor_id` | [docs](https://docs.parallel.ai/api-reference/monitor/delete-monitor) |
| [Extend FindAll Run](actions/extend-find-all-run.md) | `POST /v1beta/findall/runs/:findall_id/extend` | [docs](https://docs.parallel.ai/api-reference/findall-api-beta/extend-findall-run) |
| [Extract](actions/extract.md) | `POST /v1beta/extract` | [docs](https://docs.parallel.ai/api-reference/extract-beta/extract) |
| [Fetch Task Group Runs](actions/fetch-task-group-runs.md) | `GET /v1beta/tasks/groups/:taskgroup_id/runs` | [docs](https://docs.parallel.ai/api-reference/task-groups-beta/fetch-task-group-runs) |
| [Get FindAll Run Schema](actions/get-find-all-run-schema.md) | `GET /v1beta/findall/runs/:findall_id/schema` | [docs](https://docs.parallel.ai/api-reference/findall-api-beta/get-findall-run-schema) |
| [Ingest FindAll Run](actions/ingest-find-all-run.md) | `POST /v1beta/findall/ingest` | [docs](https://docs.parallel.ai/api-reference/findall-api-beta/ingest-findall-run) |
| [List Monitor Events](actions/list-monitor-events.md) | `GET /v1alpha/monitors/:monitor_id/events` | [docs](https://docs.parallel.ai/api-reference/monitor/list-events) |
| [List Monitors](actions/list-monitors.md) | `GET /v1alpha/monitors` | [docs](https://docs.parallel.ai/api-reference/monitor/list-monitors) |
| [List Monitors By Cursor](actions/list-monitors-by-cursor.md) | `GET /v1alpha/monitors/list` | [docs](https://docs.parallel.ai/api-reference/monitor/list-monitors) |
| [Retrieve Event Group](actions/retrieve-event-group.md) | `GET /v1alpha/monitors/:monitor_id/event_groups/:event_group_id` | [docs](https://docs.parallel.ai/api-reference/monitor/retrieve-event-group) |
| [Retrieve FindAll Run Result](actions/retrieve-find-all-run-result.md) | `GET /v1beta/findall/runs/:findall_id/result` | [docs](https://docs.parallel.ai/api-reference/findall-api-beta/findall-run-result) |
| [Retrieve FindAll Run Status](actions/retrieve-find-all-run-status.md) | `GET /v1beta/findall/runs/:findall_id` | [docs](https://docs.parallel.ai/api-reference/findall-api-beta/retrieve-findall-run-status) |
| [Retrieve Monitor](actions/retrieve-monitor.md) | `GET /v1alpha/monitors/:monitor_id` | [docs](https://docs.parallel.ai/api-reference/monitor/retrieve-monitor) |
| [Retrieve Task Group](actions/retrieve-task-group.md) | `GET /v1beta/tasks/groups/:taskgroup_id` | [docs](https://docs.parallel.ai/api-reference/task-groups-beta/retrieve-task-group) |
| [Retrieve Task Group Run](actions/retrieve-task-group-run.md) | `GET /v1beta/tasks/groups/:taskgroup_id/runs/:run_id` | [docs](https://docs.parallel.ai/api-reference/task-groups-beta/retrieve-task-group-run) |
| [Retrieve Task Run](actions/retrieve-task-run.md) | `GET /v1/tasks/runs/:run_id` | [docs](https://docs.parallel.ai/api-reference/tasks-v1/retrieve-task-run) |
| [Retrieve Task Run Input](actions/retrieve-task-run-input.md) | `GET /v1/tasks/runs/:run_id/input` | [docs](https://docs.parallel.ai/api-reference/tasks-v1/retrieve-task-run-input) |
| [Retrieve Task Run Result](actions/retrieve-task-run-result.md) | `GET /v1/tasks/runs/:run_id/result` | [docs](https://docs.parallel.ai/api-reference/tasks-v1/retrieve-task-run-result) |
| [Search](actions/search.md) | `POST /v1beta/search` | [docs](https://docs.parallel.ai/api-reference/search-beta/search) |
| [Simulate Monitor Event](actions/simulate-monitor-event.md) | `POST /v1alpha/monitors/:monitor_id/simulate_event` | [docs](https://docs.parallel.ai/api-reference/monitor/simulate-event) |
| [Stream FindAll Events](actions/stream-find-all-events.md) | `GET /v1beta/findall/runs/:findall_id/events` | [docs](https://docs.parallel.ai/api-reference/findall-api-beta/stream-findall-events) |
| [Stream Task Group Events](actions/stream-task-group-events.md) | `GET /v1beta/tasks/groups/:taskgroup_id/events` | [docs](https://docs.parallel.ai/api-reference/task-groups-beta/stream-task-group-events) |
| [Stream Task Run Events](actions/stream-task-run-events.md) | `GET /v1/tasks/runs/:run_id/events` | [docs](https://docs.parallel.ai/api-reference/tasks-v1/stream-task-run-events) |
| [Stream Task Run Events Beta](actions/stream-task-run-events-beta.md) | `GET /v1beta/tasks/runs/:run_id/events` | [docs](https://docs.parallel.ai/api-reference/tasks-v1/stream-task-run-events) |
| [Update Monitor](actions/update-monitor.md) | `POST /v1alpha/monitors/:monitor_id` | [docs](https://docs.parallel.ai/api-reference/monitor/update-monitor) |
