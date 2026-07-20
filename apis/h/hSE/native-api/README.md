# 4HSE: Native API Reference

A consolidated summary of 4HSE's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.4hse.com/en/dev/guides/using-rest-api/
- **API base URL:** `https://service.4hse.com`

## Authentication

### OAuth2 Password Grant

Authenticate with a 4HSE username and password through the documented OAuth2 password flow.

### Credentials

- **Username:** `username` · required · 4HSE username used for the OAuth2 password grant.
- **Password:** `password` · required · 4HSE password used for the OAuth2 password grant.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://auth.4hse.com/realms/4hse/protocol/openid-connect/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `profile email`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://auth.4hse.com/realms/4hse/protocol/openid-connect/token. A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.4hse.com/en/dev/guides/using-rest-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per-page` in the request body to set the page size (default 100; minimum 1). Use `page` in the request body to choose the page; numbering starts at 1.

## Filtering

Send filters in the request body. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the request body. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Person To Work Group](actions/assign-person-to-work-group.md) | `POST /v2/work-group-person/create` | [docs](https://docs.4hse.com/en/api/workgroupperson/#operation-createWorkGroupPerson-post) |
| [Create Action](actions/create-action.md) | `POST /v2/action/create` | [docs](https://docs.4hse.com/en/api/action/#operation-createAction-post) |
| [Create Action Session](actions/create-action-session.md) | `POST /v2/action-session/create` | [docs](https://docs.4hse.com/en/api/actionsession/#operation-createActionSession-post) |
| [Create Action Subscription](actions/create-action-subscription.md) | `POST /v2/action-subscription/create` | [docs](https://docs.4hse.com/en/api/actionsubscription/#operation-createActionSubscription-post) |
| [Create Certificate](actions/create-certificate.md) | `POST /v2/certificate/create` | [docs](https://docs.4hse.com/en/api/certificate/#operation-createCertificate-post) |
| [Create Certificate Action Link](actions/create-certificate-action-link.md) | `POST /v2/certificate-action/create` | [docs](https://docs.4hse.com/en/api/certificateaction/#operation-createCertificateAction-post) |
| [Create Demand](actions/create-demand.md) | `POST /v2/demand/create` | [docs](https://docs.4hse.com/en/api/demand/#operation-createDemand-post) |
| [Create Incident](actions/create-incident.md) | `POST /v2/incident/create` | [docs](https://docs.4hse.com/en/api/incident/#operation-createIncident-post) |
| [Create Office](actions/create-office.md) | `POST /v2/office/create` | [docs](https://docs.4hse.com/en/api/office/#operation-createOffice-post) |
| [Create Person](actions/create-person.md) | `POST /v2/person/create` | [docs](https://docs.4hse.com/en/api/person/#operation-createPerson-post) |
| [Create PersonOffice Assignment](actions/create-person-office-assignment.md) | `POST /v2/person-office/create` | [docs](https://docs.4hse.com/en/api/personoffice/#operation-createPersonOffice-post) |
| [Create Project](actions/create-project.md) | `POST /v2/project/create` | [docs](https://docs.4hse.com/en/api/project/#operation-createProject-post) |
| [Create Session Subscription](actions/create-session-subscription.md) | `POST /v2/action-session-subscription/create` | [docs](https://docs.4hse.com/en/api/actionsessionsubscription/#operation-createActionSessionSubscription-post) |
| [Create Work Group](actions/create-work-group.md) | `POST /v2/work-group/create` | [docs](https://docs.4hse.com/en/api/workgroup/#operation-createWorkGroup-post) |
| [Historicize Person](actions/historicize-person.md) | `POST /v2/person/historicize/:id` | [docs](https://docs.4hse.com/en/api/person/#operation-historicizePerson-post) |
| [List Action Sessions](actions/list-action-sessions.md) | `POST /v2/action-session/index` | [docs](https://docs.4hse.com/en/api/actionsession/#operation-indexActionSession-post) |
| [List Action Subscriptions](actions/list-action-subscriptions.md) | `POST /v2/action-subscription/index` | [docs](https://docs.4hse.com/en/api/actionsubscription/#operation-indexActionSubscription-post) |
| [List Actions](actions/list-actions.md) | `POST /v2/action/index` | [docs](https://docs.4hse.com/en/api/action/#operation-indexAction-post) |
| [List Certificate Action Links](actions/list-certificate-action-links.md) | `POST /v2/certificate-action/index` | [docs](https://docs.4hse.com/en/api/certificateaction/#operation-indexCertificateAction-post) |
| [List Certificates](actions/list-certificates.md) | `POST /v2/certificate/index` | [docs](https://docs.4hse.com/en/api/certificate/#operation-indexCertificate-post) |
| [List Equipment](actions/list-equipment.md) | `POST /v2/equipment/index` | [docs](https://docs.4hse.com/en/api/equipment/#operation-indexEquipment-post) |
| [List Incidents](actions/list-incidents.md) | `POST /v2/incident/index` | [docs](https://docs.4hse.com/en/api/incident/#operation-indexIncident-post) |
| [List Offices](actions/list-offices.md) | `POST /v2/office/index` | [docs](https://docs.4hse.com/en/api/office/) |
| [List People](actions/list-people.md) | `POST /v2/person/index` | [docs](https://docs.4hse.com/en/api/person/#operation-indexPerson-post) |
| [List PersonOffice Assignments](actions/list-person-office-assignments.md) | `POST /v2/person-office/index` | [docs](https://docs.4hse.com/en/api/personoffice/#operation-indexPersonOffice-post) |
| [List Projects](actions/list-projects.md) | `POST /v2/project/index` | [docs](https://docs.4hse.com/en/api/project/#operation-indexProject-post) |
| [List Session Subscriptions](actions/list-session-subscriptions.md) | `POST /v2/action-session-subscription/index` | [docs](https://docs.4hse.com/en/api/actionsessionsubscription/#operation-indexActionSessionSubscription-post) |
| [List Work Groups](actions/list-work-groups.md) | `POST /v2/work-group/index` | [docs](https://docs.4hse.com/en/api/workgroup/#operation-indexWorkGroup-post) |
| [Update Action](actions/update-action.md) | `PUT /v2/action/update/:id` | [docs](https://docs.4hse.com/en/api/action/#operation-updateAction-put) |
| [Update Action Session](actions/update-action-session.md) | `PUT /v2/action-session/update/:id` | [docs](https://docs.4hse.com/en/api/actionsession/#operation-updateActionSession-put) |
| [Update Action Subscription](actions/update-action-subscription.md) | `PUT /v2/action-subscription/update/:id` | [docs](https://docs.4hse.com/en/api/actionsubscription/#operation-updateActionSubscription-put) |
| [Update Certificate](actions/update-certificate.md) | `PUT /v2/certificate/update/:id` | [docs](https://docs.4hse.com/en/api/certificate/#operation-updateCertificate-put) |
| [Update Office](actions/update-office.md) | `PUT /v2/office/update/:id` | [docs](https://docs.4hse.com/en/api/office/#operation-updateOffice-put) |
| [Update Person](actions/update-person.md) | `PUT /v2/person/update/:id` | [docs](https://docs.4hse.com/en/api/person/#operation-updatePerson-put) |
| [Update PersonOffice Assignment](actions/update-person-office-assignment.md) | `PUT /v2/person-office/update/:id` | [docs](https://docs.4hse.com/en/api/personoffice/#operation-updatePersonOffice-put) |
| [Update Project](actions/update-project.md) | `PUT /v2/project/update/:id` | [docs](https://docs.4hse.com/en/api/project/#operation-updateProject-put) |
| [View Action](actions/view-action.md) | `GET /v2/action/view/:id` | [docs](https://docs.4hse.com/en/api/action/#operation-viewAction-get) |
| [View Certificate](actions/view-certificate.md) | `GET /v2/certificate/view/:id` | [docs](https://docs.4hse.com/en/api/certificate/#operation-viewCertificate-get) |
| [View Office](actions/view-office.md) | `GET /v2/office/view/:id` | [docs](https://docs.4hse.com/en/api/office/#operation-viewOffice-get) |
| [View Person](actions/view-person.md) | `GET /v2/person/view/:id` | [docs](https://docs.4hse.com/en/api/person/#operation-viewPerson-get) |
