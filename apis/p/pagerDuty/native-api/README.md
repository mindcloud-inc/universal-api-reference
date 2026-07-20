# PagerDuty: Native API Reference

A consolidated summary of PagerDuty's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://developer.pagerduty.com/api-reference/
- **OpenAPI specification:** https://raw.githubusercontent.com/PagerDuty/api-schema/main/reference/REST/openapiv3.json
- **API base URL:** `https://api.pagerduty.com`

## Authentication

### OAuth 2.0

Connect using PagerDuty scoped OAuth with the client credentials flow. Incident updates also require a valid PagerDuty user email for the From header.

### Credentials

- **Client ID:** `clientId` · required · PagerDuty OAuth client ID from your registered app.
- **Client Secret:** `clientSecret` · required · PagerDuty OAuth client secret from your registered app.
- **Subdomain:** `subDomain` · required · Your PagerDuty account subdomain, without .pagerduty.com.
- **Region:** `region` · optional · PagerDuty account region. Use us unless your account is hosted elsewhere.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://identity.pagerduty.com/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `as_account-us.{{credentials.subDomain}} abilities.read analytics.read change_events.read escalation_policies.read incidents.read incidents.write oncalls.read schedules.read services.read services.write standards.read teams.read users.read vendors.read`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://developer.pagerduty.com/docs/f59fdbd94ceab-o-auth-functionality)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.pagerduty+json;version=2` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25). Use `offset` in the query string as the record offset.

## Sorting

Set the sort field with `sort_by` in the query string. Only one sort field is accepted.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Incident](actions/create-incident.md) | `POST /incidents` | [docs](https://developer.pagerduty.com/api-reference/createIncident) |
| [Create Service](actions/create-service.md) | `POST /services` | [docs](https://developer.pagerduty.com/api-reference/createService) |
| [Delete Service](actions/delete-service.md) | `DELETE /services/:id` | [docs](https://developer.pagerduty.com/api-reference/deleteService) |
| [List Abilities](actions/list-abilities.md) | `GET /abilities` | [docs](https://developer.pagerduty.com/api-reference/listAbilities) |
| [List Escalation Policies](actions/list-escalation-policies.md) | `GET /escalation_policies` | [docs](https://developer.pagerduty.com/api-reference/listEscalationPolicies) |
| [List Incidents](actions/list-incidents.md) | `GET /incidents` | [docs](https://developer.pagerduty.com/api-reference/listIncidents) |
| [List On-Calls](actions/list-on-calls.md) | `GET /oncalls` | [docs](https://developer.pagerduty.com/api-reference/listOnCalls) |
| [List Schedules](actions/list-schedules.md) | `GET /schedules` | [docs](https://developer.pagerduty.com/api-reference/listSchedules) |
| [List Services](actions/list-services.md) | `GET /services` | [docs](https://developer.pagerduty.com/api-reference/listServices) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://developer.pagerduty.com/api-reference/listTeams) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developer.pagerduty.com/api-reference/listUsers) |
| [Update Incident](actions/update-incident.md) | `PUT /incidents/:id` | [docs](https://developer.pagerduty.com/api-reference/updateIncident) |
| [Update Service](actions/update-service.md) | `PUT /services/:id` | [docs](https://developer.pagerduty.com/api-reference/updateService) |
