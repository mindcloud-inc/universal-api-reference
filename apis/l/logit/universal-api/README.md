# <img src="https://images.mindcloud.co/apps/icons/logit_1774907660352.png" alt="Logit logo" width="28" height="28"> Logit: Universal API

Manage Logit accounts, stacks, alerting, and pipeline configuration

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/logit/latest
- **Category:** IT Operations / Observability
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://logit.io
- **Vendor API docs:** https://logit.io/docs/developer-api/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Logit. |

### Account Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Settings](actions/get-account-settings.md) | GET | Retrieves account settings from Logit. |

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Create Stack Alert Rule](actions/create-stack-alert-rule.md) | POST | Creates a new stack alert rule in Logit. |
| [Delete Stack Alert Rule](actions/delete-stack-alert-rule.md) | DELETE | Deletes an existing stack alert rule from Logit. |
| [Get Stack Alert Rule](actions/get-stack-alert-rule.md) | GET | Retrieves a stack alert rule from Logit. |
| [Get Stack Alert Rule Status](actions/get-stack-alert-rule-status.md) | GET | Retrieves stack alert rule status from Logit. |
| [List Alert Rule Templates](actions/list-alert-rule-templates.md) | GET | Retrieves alert rule templates from Logit. |
| [List Stack Alerting Rules](actions/list-stack-alerting-rules.md) | GET | Retrieves stack alerting rules from Logit. |
| [Test Stack Alert Rule](actions/test-stack-alert-rule.md) | GET | Tests a stack alert rule in Logit. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Stack Audit Log](actions/get-stack-audit-log.md) | GET | Retrieves a stack audit log from Logit. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Stack Ingestion Events](actions/get-stack-ingestion-events.md) | GET | Retrieves stack ingestion events from Logit. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Stack Ingestion Latency](actions/get-stack-ingestion-latency.md) | GET | Retrieves stack ingestion latency from Logit. |
| [Get Stack Ingestion Metrics](actions/get-stack-ingestion-metrics.md) | GET | Retrieves stack ingestion metrics from Logit. |
| [Get Stack Ingestion Spans](actions/get-stack-ingestion-spans.md) | GET | Retrieves stack ingestion spans from Logit. |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [Apply Stack Pipeline Config](actions/apply-stack-pipeline-config.md) | PUT | Updates stack pipeline config in Logit. |
| [Get Stack Pipeline Config](actions/get-stack-pipeline-config.md) | GET | Retrieves stack pipeline config from Logit. |
| [Get Stack Pipeline Config Validation](actions/get-stack-pipeline-config-validation.md) | GET | Retrieves stack pipeline validation status from Logit. |
| [Restart Stack Pipeline](actions/restart-stack-pipeline.md) | PUT | Restarts a stack pipeline in Logit. |
| [Validate Stack Pipeline Config](actions/validate-stack-pipeline-config.md) | GET | Validates stack pipeline config in Logit. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Stack Diagnostics](actions/get-stack-diagnostics.md) | GET | Retrieves stack diagnostics from Logit. |
| [Get Stack Ingestion History](actions/get-stack-ingestion-history.md) | GET | Retrieves stack ingestion history from Logit. |

### Stack

| Action | Method | Description |
| --- | --- | --- |
| [Get Stack Overview](actions/get-stack-overview.md) | GET | Retrieves a stack overview from Logit. |
| [List Account Stacks](actions/list-account-stacks.md) | GET | Retrieves stacks for an account from Logit. |

### Stack Connection Detail

| Action | Method | Description |
| --- | --- | --- |
| [Get Stack Connection Details](actions/get-stack-connection-details.md) | GET | Retrieves stack connection details from Logit. |

### Stack Security

| Action | Method | Description |
| --- | --- | --- |
| [Get Stack Security](actions/get-stack-security.md) | GET | Retrieves stack security details from Logit. |

### Stack Statistic

| Action | Method | Description |
| --- | --- | --- |
| [Get Stack Statistics](actions/get-stack-statistics.md) | GET | Retrieves stack statistics from Logit. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Stack Alerting Status](actions/get-stack-alerting-status.md) | GET | Retrieves stack alerting status from Logit. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Account Teams](actions/list-account-teams.md) | GET | Retrieves teams for an account from Logit. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves your profile from Logit. |
| [List Account Users](actions/list-account-users.md) | GET | Retrieves users for an account from Logit. |

