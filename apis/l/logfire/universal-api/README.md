# <img src="https://images.mindcloud.co/apps/icons/logo-logfire-sistemas-prevencao-incendios-160px_1776193410776.png" alt="Logfire logo" width="28" height="28"> Logfire: Universal API

Query Pydantic Logfire project data with SQL through the Logfire Query API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/logfire/latest
- **Category:** IT Operations / Observability
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pydantic.dev/logfire
- **Vendor API docs:** https://pydantic.dev/docs/logfire/manage/query-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Run Query](actions/run-query.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logfire/latest/actions/run-query?connectionId=$CONNECTION_ID&sql=SELECT%20start_timestamp%2C%20message%20FROM%20records%20LIMIT%2010" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [List Metrics](actions/list-metrics.md) | GET | Retrieves metrics from Logfire. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [List Exceptions](actions/list-exceptions.md) | GET | Retrieves exceptions from Logfire. |
| [List Recent Logs](actions/list-recent-logs.md) | GET | Retrieves recent logs from Logfire. |
| [List Recent Records](actions/list-recent-records.md) | GET | Retrieves recent records from Logfire. |
| [List Recent Spans](actions/list-recent-spans.md) | GET | Retrieves recent spans from Logfire. |
| [List Warnings And Errors](actions/list-warnings-and-errors.md) | GET | Retrieves warnings and errors from Logfire. |
| [Run Query](actions/run-query.md) | GET | Runs a query against Logfire data. |

