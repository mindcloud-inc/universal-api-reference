# FutureAGI: Native API Reference

A consolidated summary of FutureAGI's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://docs.futureagi.com/docs/api
- **API base URL:** `https://api.futureagi.com`

## Authentication

### API Key + Secret

Use the FutureAGI API key and secret key from the dashboard keys page.

### Credentials

- **API Key:** `apiKey` · required · Your FutureAGI API key.
- **Secret Key:** `secretKey` · required · Your FutureAGI secret key.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
X-Secret-Key: <secretKey>
```

[Official authentication documentation](https://docs.futureagi.com/docs/api/agent-definitions/listagentdefinitions)

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Export Queue](actions/export-queue.md) | `GET /model-hub/annotation-queues/:id/export/` | [docs](https://docs.futureagi.com/docs/api/annotations/queues/export) |
| [Find Queues For Source](actions/find-queues-for-source.md) | `GET /model-hub/annotation-queues/for-source/` | [docs](https://docs.futureagi.com/docs/api/annotations/queues/find-queues-for-source) |
| [Get Agent Definition](actions/get-agent-definition.md) | `GET /simulate/agent-definitions/:agentId/` | [docs](https://docs.futureagi.com/docs/api/agent-definitions/getagentdefinition) |
| [Get Agent Version](actions/get-agent-version.md) | `GET /simulate/agent-definitions/:agentId/versions/:versionId/` | [docs](https://docs.futureagi.com/docs/api/agent-versions/getagentversion) |
| [Get Annotate Detail](actions/get-annotate-detail.md) | `GET /model-hub/annotation-queues/:queueId/items/:itemId/annotate-detail/` | [docs](https://docs.futureagi.com/docs/api/annotations/items/get-annotate-detail) |
| [Get Custom Eval Config](actions/get-custom-eval-config.md) | `GET /tracer/custom-eval-config/:id/` | [docs](https://docs.futureagi.com/docs/api/custom-eval-configs/get-custom-eval-config) |
| [Get Eval Log Details](actions/get-eval-log-details.md) | `GET /model-hub/get-eval-logs-details/` | [docs](https://docs.futureagi.com/docs/api/eval-logs-metrics/getevallogdetails) |
| [Get Item Annotations](actions/get-item-annotations.md) | `GET /model-hub/annotation-queues/:queueId/items/:itemId/annotations/` | [docs](https://docs.futureagi.com/docs/api/annotations/items/get-item-annotations) |
| [Get Label](actions/get-label.md) | `GET /model-hub/annotations-labels/:id/` | [docs](https://docs.futureagi.com/docs/api/annotations/labels/get-label) |
| [Get Next Queue Item](actions/get-next-queue-item.md) | `GET /model-hub/annotation-queues/:queueId/items/next-item/` | [docs](https://docs.futureagi.com/docs/api/annotations/items/get-next-item) |
| [Get Queue](actions/get-queue.md) | `GET /model-hub/annotation-queues/:id/` | [docs](https://docs.futureagi.com/docs/api/annotations/queues/get-queue) |
| [Get Queue Agreement](actions/get-queue-agreement.md) | `GET /model-hub/annotation-queues/:id/agreement/` | [docs](https://docs.futureagi.com/docs/api/annotations/queues/get-agreement) |
| [Get Queue Analytics](actions/get-queue-analytics.md) | `GET /model-hub/annotation-queues/:id/analytics/` | [docs](https://docs.futureagi.com/docs/api/annotations/queues/get-analytics) |
| [Get Queue Progress](actions/get-queue-progress.md) | `GET /model-hub/annotation-queues/:id/progress/` | [docs](https://docs.futureagi.com/docs/api/annotations/queues/get-progress) |
| [Get Scenario Details](actions/get-scenario-details.md) | `GET /simulate/scenarios/:scenarioId/` | [docs](https://docs.futureagi.com/docs/api/scenarios/getscenario) |
| [Get Scores For Source](actions/get-scores-for-source.md) | `GET /model-hub/scores/for-source/` | [docs](https://docs.futureagi.com/docs/api/annotations/scores/get-scores-for-source) |
| [Get Simulation Analytics](actions/get-simulation-analytics.md) | `GET /sdk/api/v1/simulation/analytics/` | [docs](https://docs.futureagi.com/docs/api/simulation-analytics/analytics) |
| [Get Simulation Metrics](actions/get-simulation-metrics.md) | `GET /sdk/api/v1/simulation/metrics/` | [docs](https://docs.futureagi.com/docs/api/simulation-analytics/metrics) |
| [Get Simulation Runs](actions/get-simulation-runs.md) | `GET /sdk/api/v1/simulation/runs/` | [docs](https://docs.futureagi.com/docs/api/simulation-analytics/runs) |
| [Get Version Call Executions](actions/get-version-call-executions.md) | `GET /simulate/agent-definitions/:agentId/versions/:versionId/call-executions/` | [docs](https://docs.futureagi.com/docs/api/agent-versions/getversioncallexecutions) |
| [Get Version Eval Summary](actions/get-version-eval-summary.md) | `GET /simulate/agent-definitions/:agentId/versions/:versionId/eval-summary/` | [docs](https://docs.futureagi.com/docs/api/agent-versions/getversionevalsummary) |
| [Health Check](actions/health-check.md) | `GET /health/` | [docs](https://docs.futureagi.com/docs/api/health/healthcheck) |
| [List Agent Definitions](actions/list-agent-definitions.md) | `GET /simulate/agent-definitions/` | [docs](https://docs.futureagi.com/docs/api/agent-definitions/listagentdefinitions) |
| [List Agent Definitions](actions/list-agent-definitions2.md) | `GET /simulate/agent-definitions/` | [docs](https://docs.futureagi.com/docs/api/agent-definitions/listagentdefinitions) |
| [List Agent Versions](actions/list-agent-versions.md) | `GET /simulate/agent-definitions/:agentId/versions/` | [docs](https://docs.futureagi.com/docs/api/agent-versions/listagentversions) |
| [List Custom Eval Configs](actions/list-custom-eval-configs.md) | `GET /tracer/custom-eval-config/list_custom_eval_configs/` | [docs](https://docs.futureagi.com/docs/api/custom-eval-configs/list-configs-filtered) |
| [List Eval Tasks](actions/list-eval-tasks.md) | `GET /tracer/eval-task/list_eval_tasks/` | [docs](https://docs.futureagi.com/docs/api/eval-tasks/list-eval-tasks-filtered) |
| [List Labels](actions/list-labels.md) | `GET /model-hub/annotations-labels/` | [docs](https://docs.futureagi.com/docs/api/annotations/labels/list-labels) |
| [List Queue Items](actions/list-queue-items.md) | `GET /model-hub/annotation-queues/:queueId/items/` | [docs](https://docs.futureagi.com/docs/api/annotations/items/list-items) |
| [List Queues](actions/list-queues.md) | `GET /model-hub/annotation-queues/` | [docs](https://docs.futureagi.com/docs/api/annotations/queues/list-queues) |
| [List Scenarios](actions/list-scenarios.md) | `GET /simulate/scenarios/` | [docs](https://docs.futureagi.com/docs/api/scenarios/listscenarios) |
| [List Scores](actions/list-scores.md) | `GET /model-hub/scores/` | [docs](https://docs.futureagi.com/docs/api/annotations/scores/list-scores) |
