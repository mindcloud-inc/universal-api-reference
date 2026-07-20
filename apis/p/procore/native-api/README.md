# Procore: Native API Reference

A consolidated summary of Procore's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://developers.procore.com/reference/rest/docs/rest-api-overview
- **API base URL:** `https://api.procore.com`

## Authentication

### OAuth 2.0

Connect Procore using OAuth 2.0 authorization code flow.

### Credentials

- **Procore Company ID:** `companyId` · required · Required Procore company identifier used for the Procore-Company-Id request header on company-scoped endpoints.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.procore.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.procore.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.procore.com/oauth/token.

[Official authentication documentation](https://developers.procore.com/documentation/oauth-auth-grant-flow)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Action Plan](actions/create-action-plan.md) | `POST /rest/v1.0/projects/:project_id/action_plans/plans` | [docs](https://developers.procore.com/reference/rest/action-plans#create-action-plan) |
| [Create Change Event](actions/create-change-event.md) | `POST /rest/v1.1/change_events` | [docs](https://developers.procore.com/reference/rest/change-events#create-change-event) |
| [Create Incident](actions/create-incident.md) | `POST /rest/v1.0/projects/:project_id/incidents` | [docs](https://developers.procore.com/reference/rest/incidents#create-incident) |
| [Get Budget Metadata](actions/get-budget-metadata.md) | `GET /rest/v1.0/projects/:project_id/budget` | [docs](https://developers.procore.com/reference/rest/budget#show-budget-meta-data) |
| [Get Current User](actions/get-current-user.md) | `GET /rest/v1.0/me` | [docs](https://developers.procore.com/reference/rest/me#show-user-info) |
| [Get Form](actions/get-form.md) | `GET /rest/v1.0/projects/:project_id/forms/:id` | [docs](https://developers.procore.com/reference/rest/forms#show-form) |
| [Get Schedule Metadata](actions/get-schedule-metadata.md) | `GET /rest/v1.0/projects/:project_id/schedule` | [docs](https://developers.procore.com/reference/rest/schedule#get-schedule-metadata) |
| [List Action Plans](actions/list-action-plans.md) | `GET /rest/v1.0/projects/:project_id/action_plans/plans` | [docs](https://developers.procore.com/reference/rest/action-plans#list-action-plans) |
| [List Change Events](actions/list-change-events.md) | `GET /rest/v1.1/change_events` | [docs](https://developers.procore.com/reference/rest/change-events#list-change-events) |
| [List Commitment Contracts](actions/list-commitment-contracts.md) | `GET /rest/v2.0/companies/:company_id/projects/:project_id/commitment_contracts` | [docs](https://developers.procore.com/reference/rest/commitment-contracts#list-commitment-contracts) |
| [List Companies](actions/list-companies.md) | `GET /rest/v1.0/companies` | [docs](https://developers.procore.com/reference/rest/companies#list-companies) |
| [List Company Users](actions/list-company-users.md) | `GET /rest/v1.0/companies/[:company_id]/users` |  |
| [List Company Vendors](actions/list-company-vendors.md) | `GET /rest/v1.0/vendors` | [docs](https://developers.procore.com/reference/rest/company-vendors#list-company-vendors) |
| [List Drawing Areas](actions/list-drawing-areas.md) | `GET /rest/v1.1/projects/:project_id/drawing_areas` | [docs](https://developers.procore.com/reference/rest/drawing-areas#list-drawing-areas) |
| [List Drawings](actions/list-drawings.md) | `GET /rest/v1.1/drawing_areas/:drawing_area_id/drawings` | [docs](https://developers.procore.com/reference/rest/drawings#list-drawings) |
| [List Incidents](actions/list-incidents.md) | `GET /rest/v1.0/projects/:project_id/incidents` | [docs](https://developers.procore.com/reference/rest/incidents#list-incidents) |
| [List Observations](actions/list-observations.md) | `GET /rest/v1.0/observations/items` | [docs](https://developers.procore.com/reference/rest/observations#list-observation-items) |
| [List Project Documents](actions/list-project-documents.md) | `GET /rest/v2.0/projects/:project_id/documents` | [docs](https://developers.procore.com/reference/rest/documents#project-folder-and-file-index) |
| [List Project Locations](actions/list-project-locations.md) | `GET /rest/v1.0/projects/:project_id/locations` | [docs](https://developers.procore.com/reference/rest/locations#list-project-locations) |
| [List Project Users](actions/list-project-users.md) | `GET /rest/v1.0/projects/[:project_id]/users` | [docs](https://developers.procore.com/reference/rest/project-users#list-project-users) |
| [List Project Vendors](actions/list-project-vendors.md) | `GET /rest/v1.1/projects/[:project_id]/vendors` | [docs](https://developers.procore.com/reference/rest/project-vendors#list-project-vendors) |
| [List Projects](actions/list-projects.md) | `GET /rest/v1.0/projects` |  |
| [List Schedule Activities](actions/list-schedule-activities.md) | `GET /rest/v2.0/companies/:company_id/projects/:project_id/schedules/:schedule_id/activities` | [docs](https://developers.procore.com/reference/rest/activities#list-activities) |
| [List Schedules](actions/list-schedules.md) | `GET /rest/v2.0/companies/:company_id/projects/:project_id/schedules` | [docs](https://developers.procore.com/reference/rest/schedules#list-schedules) |
| [List Timesheets](actions/list-timesheets.md) | `GET /rest/v1.0/projects/:project_id/timesheets` | [docs](https://developers.procore.com/reference/rest/timesheets#list-all-timesheets) |
| [Update Timesheet Status](actions/update-timesheet-status.md) | `PATCH /rest/v1.0/projects/:project_id/timesheets/update_approval` | [docs](https://developers.procore.com/reference/rest/timesheets#update-timesheet-status) |
