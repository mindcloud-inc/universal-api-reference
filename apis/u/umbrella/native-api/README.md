# Umbrella: Native API Reference

A consolidated summary of Umbrella's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://developer.cisco.com/docs/cloud-security/
- **API base URL:** `https://api.umbrella.com`

## Authentication

### Manual Bearer Token (API Key)

Paste a live Umbrella access_token here. MindCloud sends it as Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.cisco.com/docs/cloud-security/umbrella-api-api-reference-auth-token-api-token-create-authorization-token/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Active Alerts](actions/count-active-alerts.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"only_active_alerts_count":true}` | [docs](https://developer.cisco.com/docs/cloud-security/list-alerts/) |
| [Create Alert Rule](actions/create-alert-rule.md) | `POST https://api.sse.cisco.com/admin/v2/alerting/rules` | [docs](https://developer.cisco.com/docs/cloud-security/create-alert-rule/) |
| [Create User](actions/create-user.md) | `POST https://api.umbrella.com/admin/v2/users` | [docs](https://developer.cisco.com/docs/cloud-security/create-user/) |
| [Create Webhook Integration](actions/create-webhook-integration.md) | `POST https://api.sse.cisco.com/admin/v2/integrations` | [docs](https://developer.cisco.com/docs/cloud-security/create-integration/) |
| [Delete Alert Rules](actions/delete-alert-rules.md) | `DELETE https://api.sse.cisco.com/admin/v2/alerting/rules` | [docs](https://developer.cisco.com/docs/cloud-security/delete-alert-rules/) |
| [Delete Integration](actions/delete-integration.md) | `DELETE https://api.sse.cisco.com/admin/v2/integrations/:intId` | [docs](https://developer.cisco.com/docs/cloud-security/delete-integration/) |
| [Delete User](actions/delete-user.md) | `DELETE /admin/v2/users/:userId` | [docs](https://developer.cisco.com/docs/cloud-security/delete-user/) |
| [Get Alert Rule](actions/get-alert-rule.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/rules/:ruleId` | [docs](https://developer.cisco.com/docs/cloud-security/get-alert-rule/) |
| [Get Integration](actions/get-integration.md) | `GET https://api.sse.cisco.com/admin/v2/integrations/:intId` | [docs](https://developer.cisco.com/docs/cloud-security/get-integration/) |
| [Get User](actions/get-user.md) | `GET /admin/v2/users/:userId` | [docs](https://developer.cisco.com/docs/cloud-security/get-user/) |
| [List Active Alerts](actions/list-active-alerts.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"status":1}` | [docs](https://developer.cisco.com/docs/cloud-security/list-alerts/) |
| [List Active High Severity Alerts](actions/list-active-high-severity-alerts.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"status":1,"severity":1}` | [docs](https://developer.cisco.com/docs/cloud-security/list-alerts/) |
| [List Active Integrations](actions/list-active-integrations.md) | `GET https://api.sse.cisco.com/admin/v2/integrations?status=active` | [docs](https://developer.cisco.com/docs/cloud-security/list-integrations/) |
| [List Alert Rules](actions/list-alert-rules.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/rules` | [docs](https://developer.cisco.com/docs/cloud-security/list-alert-rules/) |
| [List Alerts](actions/list-alerts.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/alerts` | [docs](https://developer.cisco.com/docs/cloud-security/list-alerts/) |
| [List Alerts With Context](actions/list-alerts-with-context.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"include_context":true}` | [docs](https://developer.cisco.com/docs/cloud-security/list-alerts/) |
| [List Archived Alerts](actions/list-archived-alerts.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"status":4}` | [docs](https://developer.cisco.com/docs/cloud-security/list-alerts/) |
| [List Chrome Enterprise Integrations](actions/list-chrome-enterprise-integrations.md) | `GET https://api.sse.cisco.com/admin/v2/integrations?type=chrome-enterprise.v1` | [docs](https://developer.cisco.com/docs/cloud-security/list-integrations/) |
| [List Created Integrations](actions/list-created-integrations.md) | `GET https://api.sse.cisco.com/admin/v2/integrations?status=created` | [docs](https://developer.cisco.com/docs/cloud-security/list-integrations/) |
| [List Dismissed Alerts](actions/list-dismissed-alerts.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"status":2}` | [docs](https://developer.cisco.com/docs/cloud-security/list-alerts/) |
| [List High Severity Alerts](actions/list-high-severity-alerts.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"severity":1}` | [docs](https://developer.cisco.com/docs/cloud-security/list-alerts/) |
| [List Inactive Integrations](actions/list-inactive-integrations.md) | `GET https://api.sse.cisco.com/admin/v2/integrations?status=inactive` | [docs](https://developer.cisco.com/docs/cloud-security/list-integrations/) |
| [List Info Alerts](actions/list-info-alerts.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"severity":4}` | [docs](https://developer.cisco.com/docs/cloud-security/list-alerts/) |
| [List Integrations](actions/list-integrations.md) | `GET https://api.sse.cisco.com/admin/v2/integrations` | [docs](https://developer.cisco.com/docs/cloud-security/list-integrations/) |
| [List Intune Integrations](actions/list-intune-integrations.md) | `GET https://api.sse.cisco.com/admin/v2/integrations?type=intune.v1` | [docs](https://developer.cisco.com/docs/cloud-security/list-integrations/) |
| [List Jamf Integrations](actions/list-jamf-integrations.md) | `GET https://api.sse.cisco.com/admin/v2/integrations?type=jamf.v1` | [docs](https://developer.cisco.com/docs/cloud-security/list-integrations/) |
| [List Low Severity Alerts](actions/list-low-severity-alerts.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"severity":3}` | [docs](https://developer.cisco.com/docs/cloud-security/list-alerts/) |
| [List Medium Severity Alerts](actions/list-medium-severity-alerts.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"severity":2}` | [docs](https://developer.cisco.com/docs/cloud-security/list-alerts/) |
| [List Organizations by Email](actions/list-organizations-by-email.md) | `GET https://api.umbrella.com/admin/v2/organizations` | [docs](https://developer.cisco.com/docs/cloud-security/get-information-about-organizations/) |
| [List Resolved Alerts](actions/list-resolved-alerts.md) | `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"status":3}` | [docs](https://developer.cisco.com/docs/cloud-security/list-alerts/) |
| [List Roles](actions/list-roles.md) | `GET /admin/v2/roles` | [docs](https://developer.cisco.com/docs/cloud-security/list-roles/) |
| [List Users](actions/list-users.md) | `GET /admin/v2/users` | [docs](https://developer.cisco.com/docs/cloud-security/list-users/) |
| [List Webhook Integrations](actions/list-webhook-integrations.md) | `GET https://api.sse.cisco.com/admin/v2/integrations?type=webhook.v1` | [docs](https://developer.cisco.com/docs/cloud-security/list-integrations/) |
| [Update Alert Rule](actions/update-alert-rule.md) | `PUT https://api.sse.cisco.com/admin/v2/alerting/rules/:ruleId` | [docs](https://developer.cisco.com/docs/cloud-security/update-alert-rule/) |
| [Update Integration](actions/update-integration.md) | `PATCH https://api.sse.cisco.com/admin/v2/integrations/:intId` | [docs](https://developer.cisco.com/docs/cloud-security/update-integration/) |
