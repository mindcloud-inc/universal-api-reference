# Bookafy: Native API Reference

A consolidated summary of Bookafy's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://app.bookafy.com/api-docs/index.html
- **API base URL:** `https://app.bookafy.com/api/v2`

## Authentication

### API Key

Authenticate Bookafy API requests with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://bookafy.com/custom_api_public/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `response.staffMembers`.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | `POST /appointments` | [docs](https://app.bookafy.com/api-docs/v3/appointments_part1.yaml) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://app.bookafy.com/api-docs/v3/customers_part1.yaml) |
| [Delete Appointment](actions/delete-appointment.md) | `DELETE /appointments/:id` | [docs](https://app.bookafy.com/api-docs/v3/appointments_part2.yaml) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/:id` | [docs](https://app.bookafy.com/api-docs/v3/customers_part3.yaml) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:id` | [docs](https://app.bookafy.com/api-docs/index.html) |
| [List Appointment Types with Booking Links](actions/list-appointment-types-with-booking-links.md) | `GET /appointment_types` | [docs](https://app.bookafy.com/api-docs/v3/appointment_types.yaml) |
| [List Appointments](actions/list-appointments.md) | `GET /appointments` | [docs](https://app.bookafy.com/api-docs/v3/appointments_part1.yaml) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://app.bookafy.com/api-docs/v3/customers_part1.yaml) |
| [List Services with Details](actions/list-services-with-details.md) | `GET /services` | [docs](https://app.bookafy.com/api-docs/v3/appointment_types_services.yaml) |
| [List Staff Users](actions/list-staff-users.md) | `GET /staff_members` | [docs](https://app.bookafy.com/api-docs/v3/staff_members_part1.yaml) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /api_subscriptions` | [docs](https://app.bookafy.com/api-docs/v3/webhook_part1.yaml) |
| [Update Appointment](actions/update-appointment.md) | `PUT /appointments/:id` | [docs](https://app.bookafy.com/api-docs/v3/appointments_part2.yaml) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:id` | [docs](https://app.bookafy.com/api-docs/v3/customers_part2.yaml) |
