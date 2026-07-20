# Spike.sh: Native API Reference

A consolidated summary of Spike.sh's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://docs.spike.sh/spike-api-docs
- **API base URL:** `https://api.spike.sh`

## Authentication

### API Key

Authenticate Spike API requests with an API key from Spike Settings > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.spike.sh/spike-api-docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Service](actions/create-service.md) | `POST /services/create` |  |
| [Get Escalation](actions/get-escalation.md) | `GET /escalations/:escalationId` |  |
| [Get Organization Info](actions/get-organization-info.md) | `GET /orgs/info` |  |
| [Get Service](actions/get-service.md) | `GET /services/:counterId` |  |
| [Get User](actions/get-user.md) | `GET /users/:userId` |  |
| [Get Users](actions/get-users.md) | `GET /users` | [docs](https://docs.spike.sh/spike-api-docs) |
| [List Acknowledged Incidents](actions/list-acknowledged-incidents.md) | `GET /incidents/acknowledged` |  |
| [List Active On-Call Shifts](actions/list-active-on-call-shifts.md) | `GET /oncalls/all-active-on-call-shifts` |  |
| [List Alert Rules](actions/list-alert-rules.md) | `GET /automation/rules` |  |
| [List All Teams](actions/list-all-teams.md) | `GET /teams/get-all-teams` |  |
| [List Available Integrations](actions/list-available-integrations.md) | `GET /integrations/available` |  |
| [List Escalations](actions/list-escalations.md) | `GET /escalations` |  |
| [List Incidents](actions/list-incidents.md) | `GET /incidents` |  |
| [List Integrations](actions/list-integrations.md) | `GET /integrations` |  |
| [List My Teams](actions/list-my-teams.md) | `GET /teams/get-my-teams` |  |
| [List On-Calls](actions/list-on-calls.md) | `GET /on-calls` |  |
| [List Organization Members](actions/list-organization-members.md) | `GET /orgs/members` |  |
| [List Service Incidents](actions/list-service-incidents.md) | `GET /services/:counterId/incidents` |  |
| [List Service Integrations](actions/list-service-integrations.md) | `GET /services/:counterId/integrations` |  |
| [List Services](actions/list-services.md) | `GET /services` |  |
| [List Triggered Incidents](actions/list-triggered-incidents.md) | `GET /incidents/triggered` |  |
| [Update Service](actions/update-service.md) | `PUT /services/:counterId/update` |  |
