# <img src="https://images.mindcloud.co/apps/icons/image-2892_1795548521437.png" alt="Celigo logo" width="28" height="28"> Celigo: Universal API

Celigo: Monitor, run, and troubleshoot integration flows, jobs, and errors

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/celigo/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.celigo.com
- **Vendor API docs:** https://developer.celigo.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Token Info](actions/get-token-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-token-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [List Audit Logs](actions/list-audit-logs.md) | GET |  |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Get Connection](actions/get-connection.md) | GET |  |
| [List Connections](actions/list-connections.md) | GET |  |

### Connection Test

| Action | Method | Description |
| --- | --- | --- |
| [Ping Connection](actions/ping-connection.md) | PUT |  |

### Execution Log Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Flow Run Execution Logs](actions/list-flow-run-execution-logs.md) | GET |  |

### Export

| Action | Method | Description |
| --- | --- | --- |
| [List Exports](actions/list-exports.md) | GET |  |

### Flow

| Action | Method | Description |
| --- | --- | --- |
| [Get Flow](actions/get-flow.md) | GET |  |
| [List Flows](actions/list-flows.md) | GET |  |

### Flow Error Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Flow Error Summary](actions/get-flow-error-summary.md) | GET |  |

### Flow Step Error

| Action | Method | Description |
| --- | --- | --- |
| [List Open Errors](actions/list-open-errors.md) | GET |  |
| [List Resolved Errors](actions/list-resolved-errors.md) | GET |  |

### Import

| Action | Method | Description |
| --- | --- | --- |
| [List Imports](actions/list-imports.md) | GET |  |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration](actions/get-integration.md) | GET |  |
| [List Integrations](actions/list-integrations.md) | GET |  |

### Integration Error Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration Error Summary](actions/get-integration-error-summary.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Job](actions/cancel-job.md) | PUT |  |
| [Get Job](actions/get-job.md) | GET |  |
| [List Jobs](actions/list-jobs.md) | GET |  |
| [List Latest Flow Jobs](actions/list-latest-flow-jobs.md) | GET |  |

### Job Family

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Family](actions/get-job-family.md) | GET |  |

### Token Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Info](actions/get-token-info.md) | GET |  |

