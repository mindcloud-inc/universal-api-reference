# <img src="https://images.mindcloud.co/apps/icons/dev-cycle_1775160737199.png" alt="DevCycle logo" width="28" height="28"> DevCycle: Universal API

Manage DevCycle projects, environments, features, variables, audiences, metrics, webhooks, and related configuration through the DevCycle Management API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/devCycle/latest
- **Category:** IT Operations / DevOps
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://devcycle.com
- **Vendor API docs:** https://docs.devcycle.com/management-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Environments](actions/list-environments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-environments?connectionId=$CONNECTION_ID&limit=25&offset=0&project=mindcloud" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Audiences

| Action | Method | Description |
| --- | --- | --- |
| [List Audiences](actions/list-audiences.md) | GET | Retrieves audiences from DevCycle. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [List Feature Audit Entries](actions/list-feature-audit-entries.md) | GET | Retrieves audit entries for a feature from DevCycle. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Property](actions/get-custom-property.md) | GET | Retrieves a custom property from DevCycle. |
| [Get Variable](actions/get-variable.md) | GET | Retrieves a variable from DevCycle. |
| [List Custom Properties](actions/list-custom-properties.md) | GET | Retrieves custom properties from DevCycle. |
| [List Variables](actions/list-variables.md) | GET | Retrieves variables from DevCycle. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Feature Overrides](actions/get-feature-overrides.md) | GET | Retrieves overrides for a feature from DevCycle. |
| [Get Feature Variation](actions/get-feature-variation.md) | GET | Retrieves a feature variation from DevCycle. |
| [List Feature Configurations](actions/list-feature-configurations.md) | GET | Retrieves configurations for a feature from DevCycle. |
| [List Feature Variations](actions/list-feature-variations.md) | GET | Retrieves feature variations from DevCycle. |

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [Get Environment](actions/get-environment.md) | GET | Retrieves an environment from DevCycle. |
| [List Environments](actions/list-environments.md) | GET | Retrieves environments from DevCycle. |

### Feature Requests

| Action | Method | Description |
| --- | --- | --- |
| [Get Feature](actions/get-feature.md) | GET | Retrieves a feature from DevCycle. |
| [List Features](actions/list-features.md) | GET | Retrieves features from DevCycle. |

### Integrations

| Action | Method | Description |
| --- | --- | --- |
| [Get Dynatrace Integration](actions/get-dynatrace-integration.md) | GET | Retrieves Dynatrace integrations from DevCycle. |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [List Linked Jira Issues](actions/list-linked-jira-issues.md) | GET | Retrieves linked Jira issues for a feature from DevCycle. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Metric](actions/get-metric.md) | GET | Retrieves a metric from DevCycle. |
| [List Metric Associations](actions/list-metric-associations.md) | GET | Retrieves metric associations from DevCycle. |
| [List Metrics](actions/list-metrics.md) | GET | Retrieves metrics from DevCycle. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from DevCycle. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from DevCycle. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Feature Staleness](actions/get-feature-staleness.md) | GET | Retrieves staleness details for a feature from DevCycle. |
| [Get Feature Total Evaluations](actions/get-feature-total-evaluations.md) | GET | Retrieves total feature evaluations from DevCycle. |
| [Get Metric Results](actions/get-metric-results.md) | GET | Retrieves results for a metric from DevCycle. |
| [Get Project Evaluations](actions/get-project-evaluations.md) | GET | Retrieves project evaluations from DevCycle. |
| [Get Project Total Evaluations](actions/get-project-total-evaluations.md) | GET | Retrieves total project evaluations from DevCycle. |
| [Get Test Metric Results](actions/get-test-metric-results.md) | GET | Retrieves test metric results from DevCycle. |
| [List Project Stale Features](actions/list-project-stale-features.md) | GET | Retrieves stale features for a project from DevCycle. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from DevCycle. |

