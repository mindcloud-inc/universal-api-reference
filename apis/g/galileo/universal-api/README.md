# <img src="https://images.mindcloud.co/apps/icons/galileo-ai-logo_1776944302770.jpeg" alt="Galileo logo" width="28" height="28"> Galileo: Universal API

Galileo is an AI evaluation, observability, and protection platform for logging traces, managing projects and log streams, querying metrics, datasets, experiments, feedback, and related AI application quality signals.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/galileo/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://galileo.ai
- **Vendor API docs:** https://docs.galileo.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Alert](actions/get-project-alert.md) | GET | Retrieves an alert from a Galileo project by ID. |
| [List Project Alerts](actions/list-project-alerts.md) | GET | Finds alerts for a Galileo project. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves a dataset from Galileo by ID. |
| [Get Dataset Content](actions/get-dataset-content.md) | GET | Retrieves content for a Galileo dataset. |
| [List Datasets](actions/list-datasets.md) | GET | Finds datasets in Galileo. |
| [Query Dataset Content](actions/query-dataset-content.md) | GET | Finds content in a Galileo dataset by query. |
| [Query Dataset Versions](actions/query-dataset-versions.md) | GET | Finds versions for a Galileo dataset by query. |
| [Query Datasets](actions/query-datasets.md) | GET | Finds datasets in Galileo by query. |

### Experiments

| Action | Method | Description |
| --- | --- | --- |
| [Get Experiment](actions/get-experiment.md) | GET | Retrieves an experiment from Galileo by ID. |
| [List Experiments](actions/list-experiments.md) | GET | Finds experiments for a Galileo project. |
| [List Experiments Paginated](actions/list-experiments-paginated.md) | GET | Finds experiments for a Galileo project with pagination. |
| [Search Experiments](actions/search-experiments.md) | GET | Finds experiments in a Galileo project by filters. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Current User Groups](actions/list-current-user-groups.md) | GET | Retrieves groups for the current Galileo user. |
| [List Project Groups](actions/list-project-groups.md) | GET | Finds group collaborators for a Galileo project. |

### Healthcheck

| Action | Method | Description |
| --- | --- | --- |
| [Healthcheck](actions/healthcheck.md) | GET | Retrieves API health status from Galileo. |

### Integration Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration Status](actions/get-integration-status.md) | GET | Retrieves status for a Galileo integration. |

### Integrations

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration](actions/get-integration.md) | GET | Retrieves an integration from Galileo by name. |
| [List Available Integrations](actions/list-available-integrations.md) | GET | Finds available integration types in Galileo. |

### Log Stream

| Action | Method | Description |
| --- | --- | --- |
| [Get Log Stream](actions/get-log-stream.md) | GET | Retrieves a log stream from Galileo by ID. |
| [List Log Streams](actions/list-log-streams.md) | GET | Finds log streams for a Galileo project. |
| [List Log Streams Paginated](actions/list-log-streams-paginated.md) | GET | Finds log streams for a Galileo project with pagination. |
| [Search Log Streams](actions/search-log-streams.md) | GET | Finds log streams in a Galileo project by filters. |

### Metric Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Experiment Metric Settings](actions/get-experiment-metric-settings.md) | GET | Retrieves metric settings for a Galileo experiment. |
| [Get Log Stream Metric Settings](actions/get-log-stream-metric-settings.md) | GET | Retrieves metric settings for a Galileo log stream. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Experiment Metrics](actions/get-experiment-metrics.md) | GET | Retrieves metrics for a Galileo experiment. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Galileo by ID. |
| [List Projects](actions/list-projects.md) | GET | Finds projects in Galileo with pagination. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Get Collaborator Roles](actions/get-collaborator-roles.md) | GET | Retrieves project collaborator roles from Galileo. |

### Span

| Action | Method | Description |
| --- | --- | --- |
| [Get Span](actions/get-span.md) | GET | Retrieves a span from Galileo by ID. |
| [Query Spans](actions/query-spans.md) | GET | Finds spans in a Galileo project by filters. |

### Trace

| Action | Method | Description |
| --- | --- | --- |
| [Get Trace](actions/get-trace.md) | GET | Retrieves a trace from Galileo by ID. |
| [Query Traces](actions/query-traces.md) | GET | Finds traces in a Galileo project by filters. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Galileo. |
| [List Project Users](actions/list-project-users.md) | GET | Finds user collaborators for a Galileo project. |

