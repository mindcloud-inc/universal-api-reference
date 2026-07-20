# Logit: Native API Reference

A consolidated summary of Logit's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://logit.io/docs/developer-api/api-reference/
- **OpenAPI specification:** https://dashboard.logit.io/api/reference/v1/logit-api-schema.json
- **API base URL:** `https://dashboard.logit.io`

## Authentication

### Dashboard API Key

Connect with a Logit dashboard API key from Profile > API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://logit.io/docs/developer-api/authentication/)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Stack Pipeline Config](actions/apply-stack-pipeline-config.md) | `PUT /api/stacks/:stackId/pipeline-config/apply` | [docs](https://logit.io/docs/developer-api/pipeline-configuration/) |
| [Create Stack Alert Rule](actions/create-stack-alert-rule.md) | `POST /api/stacks/:stackId/alerting/rules` | [docs](https://logit.io/docs/developer-api/alerting-via-api/) |
| [Delete Stack Alert Rule](actions/delete-stack-alert-rule.md) | `DELETE /api/stacks/:stackId/alerting/rules/:ruleId` | [docs](https://logit.io/docs/developer-api/alerting-via-api/) |
| [Get Account Settings](actions/get-account-settings.md) | `GET /api/account/:accountId/settings` | [docs](https://logit.io/docs/developer-api/account-management/) |
| [Get Profile](actions/get-profile.md) | `GET /api/me/profile` | [docs](https://logit.io/docs/developer-api/profile-and-api-keys/) |
| [Get Stack Alert Rule](actions/get-stack-alert-rule.md) | `GET /api/stacks/:stackId/alerting/rules/:ruleId` | [docs](https://logit.io/docs/developer-api/alerting-via-api/) |
| [Get Stack Alert Rule Status](actions/get-stack-alert-rule-status.md) | `GET /api/stacks/:stackId/alerting/rules/:ruleId/status` | [docs](https://logit.io/docs/developer-api/alerting-via-api/) |
| [Get Stack Alerting Status](actions/get-stack-alerting-status.md) | `GET /api/stacks/:stackId/alerting/status` | [docs](https://logit.io/docs/developer-api/alerting-via-api/) |
| [Get Stack Audit Log](actions/get-stack-audit-log.md) | `GET /api/stacks/:stackId/audit-log` | [docs](https://logit.io/docs/developer-api/managing-stacks/) |
| [Get Stack Connection Details](actions/get-stack-connection-details.md) | `GET /api/stacks/:stackId/connection-details` | [docs](https://logit.io/docs/developer-api/managing-stacks/) |
| [Get Stack Diagnostics](actions/get-stack-diagnostics.md) | `GET /api/stacks/:stackId/diagnostics` | [docs](https://logit.io/docs/developer-api/security-and-diagnostics/) |
| [Get Stack Ingestion Events](actions/get-stack-ingestion-events.md) | `GET /api/stacks/:stackId/ingestion/events` | [docs](https://logit.io/docs/developer-api/ingestion-statistics/) |
| [Get Stack Ingestion History](actions/get-stack-ingestion-history.md) | `GET /api/stacks/:stackId/ingestion/history` | [docs](https://logit.io/docs/developer-api/ingestion-statistics/) |
| [Get Stack Ingestion Latency](actions/get-stack-ingestion-latency.md) | `GET /api/stacks/:stackId/ingestion/latency` | [docs](https://logit.io/docs/developer-api/ingestion-statistics/) |
| [Get Stack Ingestion Metrics](actions/get-stack-ingestion-metrics.md) | `GET /api/stacks/:stackId/ingestion/metrics` | [docs](https://logit.io/docs/developer-api/ingestion-statistics/) |
| [Get Stack Ingestion Spans](actions/get-stack-ingestion-spans.md) | `GET /api/stacks/:stackId/ingestion/spans` | [docs](https://logit.io/docs/developer-api/ingestion-statistics/) |
| [Get Stack Overview](actions/get-stack-overview.md) | `GET /api/stacks/:stackId` | [docs](https://logit.io/docs/developer-api/managing-stacks/) |
| [Get Stack Pipeline Config](actions/get-stack-pipeline-config.md) | `GET /api/stacks/:stackId/pipeline-config` | [docs](https://logit.io/docs/developer-api/pipeline-configuration/) |
| [Get Stack Pipeline Config Validation](actions/get-stack-pipeline-config-validation.md) | `GET /api/stacks/:stackId/pipeline-config/validation` | [docs](https://logit.io/docs/developer-api/pipeline-configuration/) |
| [Get Stack Security](actions/get-stack-security.md) | `GET /api/stacks/:stackId/security` | [docs](https://logit.io/docs/developer-api/security-and-diagnostics/) |
| [Get Stack Statistics](actions/get-stack-statistics.md) | `GET /api/stacks/:stackId/statistics` | [docs](https://logit.io/docs/developer-api/managing-stacks/) |
| [List Account Stacks](actions/list-account-stacks.md) | `GET /api/account/:accountId/stacks` | [docs](https://logit.io/docs/developer-api/account-management/) |
| [List Account Teams](actions/list-account-teams.md) | `GET /api/account/:accountId/teams` | [docs](https://logit.io/docs/developer-api/account-management/) |
| [List Account Users](actions/list-account-users.md) | `GET /api/account/:accountId/users` | [docs](https://logit.io/docs/developer-api/account-management/) |
| [List Accounts](actions/list-accounts.md) | `GET /api/accounts` | [docs](https://logit.io/docs/developer-api/account-management/) |
| [List Alert Rule Templates](actions/list-alert-rule-templates.md) | `GET /api/alert-rule-templates` | [docs](https://logit.io/docs/developer-api/alerting-via-api/) |
| [List Stack Alerting Rules](actions/list-stack-alerting-rules.md) | `GET /api/stacks/:stackId/alerting/rules` | [docs](https://logit.io/docs/developer-api/alerting-via-api/) |
| [Restart Stack Pipeline](actions/restart-stack-pipeline.md) | `POST /api/stacks/:stackId/pipeline/restart` | [docs](https://logit.io/docs/developer-api/pipeline-configuration/) |
| [Test Stack Alert Rule](actions/test-stack-alert-rule.md) | `POST /api/stacks/:stackId/alerting/rules/:ruleId/test` | [docs](https://logit.io/docs/developer-api/alerting-via-api/) |
| [Validate Stack Pipeline Config](actions/validate-stack-pipeline-config.md) | `POST /api/stacks/:stackId/pipeline-config/validation` | [docs](https://logit.io/docs/developer-api/pipeline-configuration/) |
