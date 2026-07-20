# Rentman: Native API Reference

A consolidated summary of Rentman's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://api.rentman.net
- **OpenAPI specification:** https://openapi-prod-openapidocumentationbucketprodf3f6f37-23pq5ujpblj3.s3.eu-west-1.amazonaws.com/1.8.1/oas.json
- **API base URL:** `https://api.rentman.net`

## Authentication

### API Token

Use a Rentman API token generated from the Integrations settings page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.rentman.io/hc/en-us/articles/360013767839-The-Rentman-API)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `next_page_url`.

## Pagination

Use `limit` in the query string to set the page size (default 300; maximum 1500). Use `cursor` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `gte`, `lt`, `lte`, `ne`.

## Sorting

Set the sort field with `sort` in the query string. Use `+` for ascending order and `-` for descending order. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | `POST /appointments` | [docs](https://api.rentman.net/#operation/createAppointment) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://api.rentman.net/#operation/createContact) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://api.rentman.net/#operation/createProject) |
| [Create Project Function](actions/create-project-function.md) | `POST /projects/:id/projectfunctions` | [docs](https://api.rentman.net/#operation/createProjectFunction) |
| [Get Appointment](actions/get-appointment.md) | `GET /appointments/:id` | [docs](https://api.rentman.net/#operation/getAppointmentItem) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://api.rentman.net/#operation/getContactItem) |
| [Get Crew](actions/get-crew.md) | `GET /crew/:id` | [docs](https://api.rentman.net/#operation/getCrewItem) |
| [Get Equipment](actions/get-equipment.md) | `GET /equipment/:id` | [docs](https://api.rentman.net/#operation/getEquipmentItem) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:id` | [docs](https://api.rentman.net/#operation/getFactuurItem) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://api.rentman.net/#operation/getProjectItem) |
| [List Appointments](actions/list-appointments.md) | `GET /appointments` | [docs](https://api.rentman.net/#operation/getAppointmentCollection) |
| [List Contact Persons](actions/list-contact-persons.md) | `GET /contacts/:id/contactpersons` | [docs](https://api.rentman.net/#operation/getContactContactPersonCollection) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://api.rentman.net/#operation/getContactCollection) |
| [List Crew](actions/list-crew.md) | `GET /crew` | [docs](https://api.rentman.net/#operation/getCrewCollection) |
| [List Crew Rates](actions/list-crew-rates.md) | `GET /rates` | [docs](https://api.rentman.net/#operation/getCrewRateCollection) |
| [List Equipment](actions/list-equipment.md) | `GET /equipment` | [docs](https://api.rentman.net/#operation/getEquipmentCollection) |
| [List Equipment Serial Numbers](actions/list-equipment-serial-numbers.md) | `GET /equipment/:id/serialnumbers` | [docs](https://api.rentman.net/#operation/getEquipmentSerialNumberCollection) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://api.rentman.net/#operation/getFactuurCollection) |
| [List Project Crew](actions/list-project-crew.md) | `GET /projects/:id/projectcrew` | [docs](https://api.rentman.net/#operation/getProjectProjectCrewCollection) |
| [List Project Equipment](actions/list-project-equipment.md) | `GET /projects/:id/projectequipment` | [docs](https://api.rentman.net/#operation/getProjectProjectEquipmentCollection) |
| [List Project Functions](actions/list-project-functions.md) | `GET /projects/:id/projectfunctions` | [docs](https://api.rentman.net/#operation/getProjectProjectFunctionCollection) |
| [List Project Subprojects](actions/list-project-subprojects.md) | `GET /projects/:id/subprojects` | [docs](https://api.rentman.net/#operation/getProjectSubprojectCollection) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://api.rentman.net/#operation/getProjectCollection) |
| [List Vehicles](actions/list-vehicles.md) | `GET /vehicles` | [docs](https://api.rentman.net/#operation/getVehicleCollection) |
| [Update Appointment](actions/update-appointment.md) | `PUT /appointments/:id` | [docs](https://api.rentman.net/#operation/updateAppointment) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://api.rentman.net/#operation/updateContact) |
