# Solace PubSub+: Native API Reference

A consolidated summary of Solace PubSub+'s API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.solace.dev/cloud/reference/using-the-v2-rest-apis-for-pubsub-cloud
- **OpenAPI specification:** https://api.solace.dev/cloud/page/openapi-specifications
- **API base URL:** `https://api.solace.cloud`

## Authentication

### Bearer API Token

Use a Solace Cloud API token as a bearer token for REST API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.solace.dev/cloud/reference/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; accepted range 1–1000). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`, `like`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get API Token](actions/get-api-token.md) | `GET /api/v2/platform/apiTokens/{tokenId}` | [docs](https://api.solace.dev/cloud/reference/gettoken) |
| [Get API Tokens](actions/get-api-tokens.md) | `GET /api/v2/platform/apiTokens` | [docs](https://api.solace.dev/cloud/reference/gettokens) |
| [Get Application](actions/get-application.md) | `GET /api/v2/architecture/applications/{id}` | [docs](https://api.solace.dev/cloud/reference/getapplication) |
| [Get Application Domain](actions/get-application-domain.md) | `GET /api/v2/architecture/applicationDomains/{id}` | [docs](https://api.solace.dev/cloud/reference/getapplicationdomain) |
| [Get Application Domains](actions/get-application-domains.md) | `GET /api/v2/architecture/applicationDomains` | [docs](https://api.solace.dev/cloud/reference/getapplicationdomains) |
| [Get Applications](actions/get-applications.md) | `GET /api/v2/architecture/applications` | [docs](https://api.solace.dev/cloud/reference/getapplications) |
| [Get Broker Service Versions](actions/get-broker-service-versions.md) | `GET /api/v2/missionControl/eventBrokerServiceVersions` | [docs](https://api.solace.dev/cloud/reference/geteventbrokerserviceversions) |
| [Get Broker State](actions/get-broker-state.md) | `GET /api/v2/missionControl/eventBrokerServices/{serviceId}/brokerState` | [docs](https://api.solace.dev/cloud/reference/getbrokerstatebyserviceid) |
| [Get Datacenter](actions/get-datacenter.md) | `GET /api/v2/missionControl/datacenters/{id}` | [docs](https://api.solace.dev/cloud/reference/getdatacenter) |
| [Get Datacenters](actions/get-datacenters.md) | `GET /api/v2/missionControl/datacenters` | [docs](https://api.solace.dev/cloud/reference/getdatacenters) |
| [Get Default Broker Versions](actions/get-default-broker-versions.md) | `GET /api/v2/missionControl/defaultBrokerVersions` | [docs](https://api.solace.dev/cloud/reference/getversions) |
| [Get Event Broker Service](actions/get-event-broker-service.md) | `GET /api/v2/missionControl/eventBrokerServices/{id}` | [docs](https://api.solace.dev/cloud/reference/getservice) |
| [Get Event Broker Services](actions/get-event-broker-services.md) | `GET /api/v2/missionControl/eventBrokerServices` | [docs](https://api.solace.dev/cloud/reference/getservices) |
| [Get Events](actions/get-events.md) | `GET /api/v2/architecture/events` | [docs](https://api.solace.dev/cloud/reference/getevents) |
| [Get Maintenance Activities](actions/get-maintenance-activities.md) | `GET /api/v2/missionControl/maintenanceActivities` | [docs](https://api.solace.dev/cloud/reference/maintenance-activities) |
| [Get Maintenance Activity](actions/get-maintenance-activity.md) | `GET /api/v2/missionControl/maintenanceActivities/{maintenanceActivityId}` | [docs](https://api.solace.dev/cloud/reference/getmaintenanceactivity) |
| [Get Maintenance Schedule](actions/get-maintenance-schedule.md) | `GET /api/v2/missionControl/maintenanceSchedules/{maintenanceScheduleId}` | [docs](https://api.solace.dev/cloud/reference/getmaintenanceschedule) |
| [Get Maintenance Schedules](actions/get-maintenance-schedules.md) | `GET /api/v2/missionControl/maintenanceSchedules` | [docs](https://api.solace.dev/cloud/reference/getmaintenanceschedules) |
| [Get Organization Contacts](actions/get-organization-contacts.md) | `GET /api/v2/platform/contacts` | [docs](https://api.solace.dev/cloud/reference/getmycontacts) |
| [Get Platform Environment](actions/get-platform-environment.md) | `GET /api/v2/platform/environments/{id}` | [docs](https://api.solace.dev/cloud/reference/getenvironmentbyid) |
| [Get Platform Environments](actions/get-platform-environments.md) | `GET /api/v2/platform/environments` | [docs](https://api.solace.dev/cloud/reference/searchenvironments) |
| [Get Resource Assignments](actions/get-resource-assignments.md) | `GET /api/v2/platform/rrbac/resourceAssignments` | [docs](https://api.solace.dev/cloud/reference/getresourceassignments) |
| [Get Roles](actions/get-roles.md) | `GET /api/v2/platform/roles` | [docs](https://api.solace.dev/cloud/reference/getroles) |
| [Get Service Class](actions/get-service-class.md) | `GET /api/v2/missionControl/serviceClasses/{id}` | [docs](https://api.solace.dev/cloud/reference/getserviceclass) |
| [Get Service Classes](actions/get-service-classes.md) | `GET /api/v2/missionControl/serviceClasses` | [docs](https://api.solace.dev/cloud/reference/getserviceclasses) |
| [Get Service Operation](actions/get-service-operation.md) | `GET /api/v2/missionControl/eventBrokerServices/{serviceId}/operations/{operationId}` | [docs](https://api.solace.dev/cloud/reference/getserviceoperation) |
| [Get Service Operations](actions/get-service-operations.md) | `GET /api/v2/missionControl/eventBrokerServices/{serviceId}/operations` | [docs](https://api.solace.dev/cloud/reference/getserviceoperations) |
| [Get User Group](actions/get-user-group.md) | `GET /api/v2/platform/userGroups/{id}` | [docs](https://api.solace.dev/cloud/reference/getusergroup) |
| [Get User Groups](actions/get-user-groups.md) | `GET /api/v2/platform/userGroups` | [docs](https://api.solace.dev/cloud/reference/getusergroups) |
| [Get Users](actions/get-users.md) | `GET /api/v2/platform/users` | [docs](https://api.solace.dev/cloud/reference/getusers) |
