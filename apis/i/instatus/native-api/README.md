# Instatus: Native API Reference

A consolidated summary of Instatus's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://instatus.com/help/api
- **API base URL:** `https://api.instatus.com`

## Authentication

### API Key

Authenticate to the Instatus API with an API token in the Authorization header.

### Credentials

- **API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://instatus.com/help/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Component](actions/create-component.md) | `POST /v1/:page_id/components` | [docs](https://instatus.com/help/api/components) |
| [Create Incident](actions/create-incident.md) | `POST /v1/:page_id/incidents` | [docs](https://instatus.com/help/api/incidents) |
| [Create Incident Update](actions/create-incident-update.md) | `POST /v1/:page_id/incidents/:incident_id/incident-updates` | [docs](https://instatus.com/help/api/incident-updates) |
| [Create Maintenance](actions/create-maintenance.md) | `POST /v1/:page_id/maintenances` | [docs](https://instatus.com/help/api/maintenances) |
| [Create Status Page](actions/create-status-page.md) | `POST /v1/pages` | [docs](https://instatus.com/help/api/status-pages) |
| [Delete Component](actions/delete-component.md) | `DELETE /v1/:page_id/components/:component_id` | [docs](https://instatus.com/help/api/components) |
| [Delete Incident](actions/delete-incident.md) | `DELETE /v1/:page_id/incidents/:incident_id` | [docs](https://instatus.com/help/api/incidents) |
| [Delete Maintenance](actions/delete-maintenance.md) | `DELETE /v1/:page_id/maintenances/:maintenance_id` | [docs](https://instatus.com/help/api/maintenances) |
| [Delete Status Page](actions/delete-status-page.md) | `DELETE /v2/:page_id` | [docs](https://instatus.com/help/api/status-pages) |
| [Get Component](actions/get-component.md) | `GET /v2/:page_id/components/:component_id` | [docs](https://instatus.com/help/api/components) |
| [Get Incident](actions/get-incident.md) | `GET /v1/:page_id/incidents/:incident_id` | [docs](https://instatus.com/help/api/incidents) |
| [Get Incident Update](actions/get-incident-update.md) | `GET /v1/:page_id/incidents/:incident_id/incident-updates/:incident_update_id` | [docs](https://instatus.com/help/api/incident-updates) |
| [Get Maintenance](actions/get-maintenance.md) | `GET /v1/:page_id/maintenances/:maintenance_id` | [docs](https://instatus.com/help/api/maintenances) |
| [Get User Profile](actions/get-user-profile.md) | `GET /v1/user` | [docs](https://instatus.com/help/api/user-profile) |
| [List Components](actions/list-components.md) | `GET /v2/:page_id/components` | [docs](https://instatus.com/help/api/components) |
| [List Incidents](actions/list-incidents.md) | `GET /v1/:page_id/incidents` | [docs](https://instatus.com/help/api/incidents) |
| [List Maintenances](actions/list-maintenances.md) | `GET /v1/:page_id/maintenances` | [docs](https://instatus.com/help/api/maintenances) |
| [List Status Pages](actions/list-status-pages.md) | `GET /v2/pages` | [docs](https://instatus.com/help/api/status-pages) |
| [List Subscribers](actions/list-subscribers.md) | `GET /v2/:page_id/subscribers` | [docs](https://instatus.com/help/api/subscribers) |
| [Update Component](actions/update-component.md) | `PUT /v2/:page_id/components/:component_id` | [docs](https://instatus.com/help/api/components) |
| [Update Incident](actions/update-incident.md) | `PUT /v1/:page_id/incidents/:incident_id` | [docs](https://instatus.com/help/api/incidents) |
| [Update Incident Update](actions/update-incident-update.md) | `PUT /v1/:page_id/incidents/:incident_id/incident-updates/:incident_update_id` | [docs](https://instatus.com/help/api/incident-updates) |
| [Update Maintenance](actions/update-maintenance.md) | `PUT /v1/:page_id/maintenances/:maintenance_id` | [docs](https://instatus.com/help/api/maintenances) |
| [Update Status Page](actions/update-status-page.md) | `PUT /v2/:page_id` | [docs](https://instatus.com/help/api/status-pages) |
