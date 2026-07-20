# <img src="https://images.mindcloud.co/apps/icons/parallel-web-systems_1775734529238.png" alt="Parallel Web Systems logo" width="28" height="28"> Parallel Web Systems: Universal API

Parallel Web Systems provides AI-powered web search, extraction, task execution, FindAll enrichment workflows, chat completions, and monitor automation through the Parallel API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/parallelWebSystems/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://parallel.ai
- **Vendor API docs:** https://docs.parallel.ai/getting-started/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Monitors](actions/list-monitors.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/list-monitors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Chat Completions](actions/chat-completions.md) | POST |  |

### Event Group

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Event Group](actions/retrieve-event-group.md) | GET |  |

### Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Extract](actions/extract.md) | POST |  |

### Findall Event

| Action | Method | Description |
| --- | --- | --- |
| [Stream FindAll Events](actions/stream-find-all-events.md) | GET |  |

### Findall Run

| Action | Method | Description |
| --- | --- | --- |
| [Add Enrichment to FindAll Run](actions/add-enrichment-to-find-all-run.md) | PUT |  |
| [Cancel FindAll Run](actions/cancel-find-all-run.md) | PUT |  |
| [Create FindAll Run](actions/create-find-all-run.md) | POST |  |
| [Extend FindAll Run](actions/extend-find-all-run.md) | PUT |  |
| [Ingest FindAll Run](actions/ingest-find-all-run.md) | POST |  |
| [Retrieve FindAll Run Status](actions/retrieve-find-all-run-status.md) | GET |  |

### Findall Run Result

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve FindAll Run Result](actions/retrieve-find-all-run-result.md) | GET |  |

### Monitor

| Action | Method | Description |
| --- | --- | --- |
| [Create Monitor](actions/create-monitor.md) | POST |  |
| [Delete Monitor](actions/delete-monitor.md) | DELETE |  |
| [List Monitors](actions/list-monitors.md) | GET |  |
| [List Monitors By Cursor](actions/list-monitors-by-cursor.md) | GET |  |
| [Retrieve Monitor](actions/retrieve-monitor.md) | GET |  |
| [Update Monitor](actions/update-monitor.md) | PUT |  |

### Monitor Event

| Action | Method | Description |
| --- | --- | --- |
| [List Monitor Events](actions/list-monitor-events.md) | GET |  |
| [Simulate Monitor Event](actions/simulate-monitor-event.md) | POST |  |

### Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get FindAll Run Schema](actions/get-find-all-run-schema.md) | GET |  |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | POST |  |

### Task Group

| Action | Method | Description |
| --- | --- | --- |
| [Add Runs to Task Group](actions/add-runs-to-task-group.md) | PUT |  |
| [Create Task Group](actions/create-task-group.md) | POST |  |
| [Retrieve Task Group](actions/retrieve-task-group.md) | GET |  |

### Task Group Event

| Action | Method | Description |
| --- | --- | --- |
| [Stream Task Group Events](actions/stream-task-group-events.md) | GET |  |

### Task Run

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Run](actions/create-task-run.md) | POST |  |
| [Fetch Task Group Runs](actions/fetch-task-group-runs.md) | GET |  |
| [Retrieve Task Group Run](actions/retrieve-task-group-run.md) | GET |  |
| [Retrieve Task Run](actions/retrieve-task-run.md) | GET |  |

### Task Run Event

| Action | Method | Description |
| --- | --- | --- |
| [Stream Task Run Events](actions/stream-task-run-events.md) | GET |  |
| [Stream Task Run Events Beta](actions/stream-task-run-events-beta.md) | GET |  |

### Task Run Input

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Task Run Input](actions/retrieve-task-run-input.md) | GET |  |

### Task Run Result

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Task Run Result](actions/retrieve-task-run-result.md) | GET |  |

