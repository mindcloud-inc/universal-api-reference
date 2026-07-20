# Fleetio: Native API Reference

A consolidated summary of Fleetio's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://developer.fleetio.com/docs/api/fleetio-developer-api
- **API base URL:** `https://secure.fleetio.com/api/`

## Authentication

### Fleetio API v2025-05-05

null

### Credentials

- **Account Token:** `accountToken` · required · Fleetio Account-Token header value from your Fleetio account settings. This is required alongside the API Key for the 2025-05-05 API.
- **API Key:** `apiKey` · required · Fleetio API Key for Developer API version 2025-05-05. Paste the raw key only; MindCloud will send it as Authorization: Token <apiKey>.

Send these headers with each API request:

```http
Account-Token: <accountToken>
```

[Official authentication documentation](https://developer.fleetio.com/docs/api/fleetio-developer-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

The next-page cursor is read from `nextCursor`. The current page number is read from `startCursor`.

## Pagination

Use `per_page` in the query string to set the page size (default 100; accepted range 2–100). Use `start_cursor` in the query string as the pagination cursor.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST contacts` | [docs](https://developer.fleetio.com/docs/api/contacts-create) |
| [Create Fuel Entry](actions/create-fuel-entry.md) | `POST fuel_entries` | [docs](https://developer.fleetio.com/docs/api/fuel-entries-create) |
| [Create Issue](actions/create-issue.md) | `POST issues` | [docs](https://developer.fleetio.com/docs/api/issues-create) |
| [Create Meter Entry](actions/create-meter-entry.md) | `POST meter_entries` | [docs](https://developer.fleetio.com/docs/api/meter-entries-create) |
| [Create Service Entry](actions/create-service-entry.md) | `POST service_entries` | [docs](https://developer.fleetio.com/docs/api/service-entries-create) |
| [Create Vehicle](actions/create-vehicle.md) | `POST vehicles` | [docs](https://developer.fleetio.com/docs/api/vehicles-create) |
| [Create Vendor](actions/create-vendor.md) | `POST vendors` | [docs](https://developer.fleetio.com/docs/api/vendors-create) |
| [Create Work Order](actions/create-work-order.md) | `POST work_orders` | [docs](https://developer.fleetio.com/docs/api/work-orders-create) |
| [Delete Contact](actions/delete-contact.md) | `DELETE contacts/:id` | [docs](https://developer.fleetio.com/docs/api/contacts-destroy) |
| [Delete Fuel Entry](actions/delete-fuel-entry.md) | `DELETE fuel_entries/:id` | [docs](https://developer.fleetio.com/docs/api/fuel-entries-destroy) |
| [Delete Issue](actions/delete-issue.md) | `DELETE issues/:id` | [docs](https://developer.fleetio.com/docs/api/issues-destroy) |
| [Delete Meter Entry](actions/delete-meter-entry.md) | `DELETE meter_entries/:id` | [docs](https://developer.fleetio.com/docs/api/meter-entries-destroy) |
| [Delete Vehicle](actions/delete-vehicle.md) | `DELETE vehicles/:id` | [docs](https://developer.fleetio.com/docs/api/vehicles-destroy) |
| [Delete Vendor](actions/delete-vendor.md) | `DELETE vendors/:id` | [docs](https://developer.fleetio.com/docs/api/vendors-destroy) |
| [Delete Work Order](actions/delete-work-order.md) | `DELETE work_orders/:id` | [docs](https://developer.fleetio.com/docs/api/work-orders-destroy) |
| [List Contacts](actions/list-contacts.md) | `GET contacts` | [docs](https://developer.fleetio.com/docs/api/contacts-index) |
| [List Fuel Entries](actions/list-fuel-entries.md) | `GET fuel_entries` | [docs](https://developer.fleetio.com/docs/api/fuel-entries-index) |
| [List Issues](actions/list-issues.md) | `GET issues` | [docs](https://developer.fleetio.com/docs/api/issues-index) |
| [List Meter Entries](actions/list-meter-entries.md) | `GET meter_entries` | [docs](https://developer.fleetio.com/docs/api/meter-entries-index) |
| [List Service Entries](actions/list-service-entries.md) | `GET service_entries` | [docs](https://developer.fleetio.com/docs/api/service-entries-index) |
| [List Vehicles](actions/list-vehicles.md) | `GET vehicles` | [docs](https://developer.fleetio.com/docs/api/vehicles-index) |
| [List Vendors](actions/list-vendors.md) | `GET vendors` | [docs](https://developer.fleetio.com/docs/api/vendors-index) |
| [List Work Orders](actions/list-work-orders.md) | `GET work_orders` | [docs](https://developer.fleetio.com/docs/api/work-orders-index) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET contacts/:id` | [docs](https://developer.fleetio.com/docs/api/contacts-show) |
| [Retrieve Fuel Entry](actions/retrieve-fuel-entry.md) | `GET fuel_entries/:id` | [docs](https://developer.fleetio.com/docs/api/fuel-entries-show) |
| [Retrieve Issue](actions/retrieve-issue.md) | `GET issues/:id` | [docs](https://developer.fleetio.com/docs/api/issues-show) |
| [Retrieve Meter Entry](actions/retrieve-meter-entry.md) | `GET meter_entries/:id` | [docs](https://developer.fleetio.com/docs/api/meter-entries-show) |
| [Retrieve Service Entry](actions/retrieve-service-entry.md) | `GET service_entries/:id` | [docs](https://developer.fleetio.com/docs/api/service-entries-show) |
| [Retrieve Vehicle](actions/retrieve-vehicle.md) | `GET vehicles/:id` | [docs](https://developer.fleetio.com/docs/api/vehicles-show) |
| [Retrieve Vendor](actions/retrieve-vendor.md) | `GET vendors/:id` | [docs](https://developer.fleetio.com/docs/api/vendors-show) |
| [Retrieve Work Order](actions/retrieve-work-order.md) | `GET work_orders/:id` | [docs](https://developer.fleetio.com/docs/api/work-orders-show) |
| [Update Contact](actions/update-contact.md) | `PATCH contacts/:id` | [docs](https://developer.fleetio.com/docs/api/contacts-update) |
| [Update Fuel Entry](actions/update-fuel-entry.md) | `PATCH fuel_entries/:id` | [docs](https://developer.fleetio.com/docs/api/fuel-entries-update) |
| [Update Issue](actions/update-issue.md) | `PATCH issues/:id` | [docs](https://developer.fleetio.com/docs/api/issues-update) |
| [Update Service Entry](actions/update-service-entry.md) | `PATCH service_entries/:id` | [docs](https://developer.fleetio.com/docs/api/service-entries-update) |
| [Update Vehicle](actions/update-vehicle.md) | `PATCH vehicles/:id` | [docs](https://developer.fleetio.com/docs/api/vehicles-update) |
| [Update Vendor](actions/update-vendor.md) | `PATCH vendors/:id` | [docs](https://developer.fleetio.com/docs/api/vendors-update) |
| [Update Work Order](actions/update-work-order.md) | `PATCH work_orders/:id` | [docs](https://developer.fleetio.com/docs/api/work-orders-update) |
