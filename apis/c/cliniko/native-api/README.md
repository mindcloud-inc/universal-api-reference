# Cliniko: Native API Reference

A consolidated summary of Cliniko's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.api.cliniko.com/
- **OpenAPI specification:** https://docs.api.cliniko.com/_bundle/openapi.json?download=
- **API base URL:** `https://api.au5.cliniko.com/v1`

## Authentication

### API Key via HTTP Basic

Use your Cliniko API key as the Basic auth username and leave the password blank.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://help.cliniko.com/en/articles/1023957-generate-a-cliniko-api-key)

## Pagination

Use `per_page` in the query string to set the page size (accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Multiple sort fields can be combined.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Appointment Type](actions/get-appointment-type.md) | `GET /appointment_types/:id` | [docs](https://docs.api.cliniko.com/openapi/appointment_type) |
| [Get Attendee](actions/get-attendee.md) | `GET /attendees/:id` | [docs](https://docs.api.cliniko.com/openapi/attendee) |
| [Get Business](actions/get-business.md) | `GET /businesses/:id` | [docs](https://docs.api.cliniko.com/openapi/business) |
| [Get Group Appointment](actions/get-group-appointment.md) | `GET /group_appointments/:id` | [docs](https://docs.api.cliniko.com/openapi/group_appointment) |
| [Get Individual Appointment](actions/get-individual-appointment.md) | `GET /individual_appointments/:id` | [docs](https://docs.api.cliniko.com/openapi/individual_appointment) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:id` | [docs](https://docs.api.cliniko.com/openapi/invoice) |
| [Get Patient](actions/get-patient.md) | `GET /patients/:id` | [docs](https://docs.api.cliniko.com/openapi/patient) |
| [Get Patient Case](actions/get-patient-case.md) | `GET /patient_cases/:id` | [docs](https://docs.api.cliniko.com/openapi/patient_case) |
| [Get Practitioner](actions/get-practitioner.md) | `GET /practitioners/:id` | [docs](https://docs.api.cliniko.com/openapi/practitioner) |
| [Get Settings](actions/get-settings.md) | `GET /settings` | [docs](https://docs.api.cliniko.com/openapi/settings) |
| [List Appointment Types](actions/list-appointment-types.md) | `GET /appointment_types` | [docs](https://docs.api.cliniko.com/openapi/appointment_type) |
| [List Attendees](actions/list-attendees.md) | `GET /attendees` | [docs](https://docs.api.cliniko.com/openapi/attendee) |
| [List Billable Items](actions/list-billable-items.md) | `GET /billable_items` | [docs](https://docs.api.cliniko.com/openapi/billable_item) |
| [List Businesses](actions/list-businesses.md) | `GET /businesses` | [docs](https://docs.api.cliniko.com/openapi/business) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://docs.api.cliniko.com/openapi/contact) |
| [List Group Appointments](actions/list-group-appointments.md) | `GET /group_appointments` | [docs](https://docs.api.cliniko.com/openapi/group_appointment) |
| [List Individual Appointments](actions/list-individual-appointments.md) | `GET /individual_appointments` | [docs](https://docs.api.cliniko.com/openapi/individual_appointment) |
| [List Invoice Items](actions/list-invoice-items.md) | `GET /invoice_items` | [docs](https://docs.api.cliniko.com/openapi/invoice_item) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://docs.api.cliniko.com/openapi/invoice) |
| [List Medical Alerts](actions/list-medical-alerts.md) | `GET /medical_alerts` | [docs](https://docs.api.cliniko.com/openapi/medical_alert) |
| [List Patient Cases](actions/list-patient-cases.md) | `GET /patient_cases` | [docs](https://docs.api.cliniko.com/openapi/patient_case) |
| [List Patients](actions/list-patients.md) | `GET /patients` | [docs](https://docs.api.cliniko.com/openapi/patient) |
| [List Practitioners](actions/list-practitioners.md) | `GET /practitioners` | [docs](https://docs.api.cliniko.com/openapi/practitioner) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://docs.api.cliniko.com/openapi/product) |
