# Samedi: Native API Reference

A consolidated summary of Samedi's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.samedi.de/booking-api/
- **API base URL:** `https://patient.samedi.de/api`

## Authentication

### OAuth 2.0

Authorize a samedi patient account for Booking API protected resources.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://patient.samedi.de/api/auth/v2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://patient.samedi.de/api/auth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `appointments:read appointments:book profile:read`.

[Official authentication documentation](https://api-docs.samedi.de/booking-api/authentication/)

## API conventions

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Book Appointment](actions/book-appointment.md) | `POST /booking/v3/book` | [docs](https://api-docs.samedi.de/booking-api/appointment-booking/) |
| [Complete Paid Appointment](actions/complete-paid-appointment.md) | `POST /booking/v3/book` | [docs](https://api-docs.samedi.de/booking-api/appointment-booking/) |
| [Create PayPal Order](actions/create-paypal-order.md) | `POST /automated_payment/v1/orders` | [docs](https://api-docs.samedi.de/booking-api/appointment-booking/) |
| [Get Current Patient User](actions/get-current-patient-user.md) | `GET /booking/v3/user` | [docs](https://api-docs.samedi.de/booking-api/appointment-data/) |
| [Get Institution Details](actions/get-institution-details.md) | `GET /booking/v3/practices/:practiceId` | [docs](https://api-docs.samedi.de/booking-api/appointment-data/) |
| [Guest Book Appointment](actions/guest-book-appointment.md) | `POST /booking/v3/book` | [docs](https://api-docs.samedi.de/booking-api/appointment-booking/) |
| [Guest Complete Paid Appointment](actions/guest-complete-paid-appointment.md) | `POST /booking/v3/book` | [docs](https://api-docs.samedi.de/booking-api/appointment-booking/) |
| [List Appointment Categories](actions/list-appointment-categories.md) | `GET /booking/v3/event_categories` | [docs](https://api-docs.samedi.de/booking-api/appointment-data/) |
| [List Appointment Types](actions/list-appointment-types.md) | `GET /booking/v3/event_types` | [docs](https://api-docs.samedi.de/booking-api/appointment-data/) |
| [List Available Days](actions/list-available-days.md) | `GET /booking/v3/dates` | [docs](https://api-docs.samedi.de/booking-api/appointment-data/) |
| [List Available Times](actions/list-available-times.md) | `GET /booking/v3/times` | [docs](https://api-docs.samedi.de/booking-api/appointment-data/) |
| [List Health Insurances](actions/list-health-insurances.md) | `GET /booking/v3/insurances` | [docs](https://api-docs.samedi.de/booking-api/insurances/) |
| [List Upcoming Patient Appointments](actions/list-upcoming-patient-appointments.md) | `GET /booking/v3/events/upcoming` | [docs](https://api-docs.samedi.de/booking-api/patient-appointments/) |
