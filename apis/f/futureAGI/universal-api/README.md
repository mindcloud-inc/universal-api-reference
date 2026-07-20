# <img src="https://images.mindcloud.co/apps/icons/futureagi-icon-padded_1775675334142.png" alt="FutureAGI logo" width="28" height="28"> FutureAGI: Universal API

FutureAGI is an AI lifecycle platform for simulation, evaluation, observability, optimization, datasets, annotations, and guardrails for agentic applications.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/futureAGI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.futureagi.com
- **Vendor API docs:** https://docs.futureagi.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agent Definitions](actions/list-agent-definitions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-agent-definitions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Export Queue](actions/export-queue.md) | GET |  |
| [Find Queues For Source](actions/find-queues-for-source.md) | GET |  |
| [Get Agent Definition](actions/get-agent-definition.md) | GET |  |
| [Get Agent Version](actions/get-agent-version.md) | GET |  |
| [Get Annotate Detail](actions/get-annotate-detail.md) | GET |  |
| [Get Custom Eval Config](actions/get-custom-eval-config.md) | GET |  |
| [Get Eval Log Details](actions/get-eval-log-details.md) | GET |  |
| [Get Item Annotations](actions/get-item-annotations.md) | GET |  |
| [Get Label](actions/get-label.md) | GET |  |
| [Get Next Queue Item](actions/get-next-queue-item.md) | GET |  |
| [Get Queue](actions/get-queue.md) | GET |  |
| [Get Queue Agreement](actions/get-queue-agreement.md) | GET |  |
| [Get Queue Analytics](actions/get-queue-analytics.md) | GET |  |
| [Get Queue Progress](actions/get-queue-progress.md) | GET |  |
| [Get Scenario Details](actions/get-scenario-details.md) | GET |  |
| [Get Scores For Source](actions/get-scores-for-source.md) | GET |  |
| [Get Simulation Analytics](actions/get-simulation-analytics.md) | GET |  |
| [Get Simulation Metrics](actions/get-simulation-metrics.md) | GET |  |
| [Get Simulation Runs](actions/get-simulation-runs.md) | GET |  |
| [Get Version Call Executions](actions/get-version-call-executions.md) | GET |  |
| [Get Version Eval Summary](actions/get-version-eval-summary.md) | GET |  |
| [Health Check](actions/health-check.md) | GET |  |
| [List Agent Definitions](actions/list-agent-definitions.md) | GET |  |
| [List Agent Definitions](actions/list-agent-definitions2.md) | GET |  |
| [List Agent Versions](actions/list-agent-versions.md) | GET |  |
| [List Custom Eval Configs](actions/list-custom-eval-configs.md) | GET |  |
| [List Eval Tasks](actions/list-eval-tasks.md) | GET |  |
| [List Labels](actions/list-labels.md) | GET |  |
| [List Queue Items](actions/list-queue-items.md) | GET |  |
| [List Queues](actions/list-queues.md) | GET |  |
| [List Scenarios](actions/list-scenarios.md) | GET |  |
| [List Scores](actions/list-scores.md) | GET |  |

