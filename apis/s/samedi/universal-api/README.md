# <img src="https://images.mindcloud.co/apps/icons/images_1776108197093.png" alt="Samedi logo" width="28" height="28"> Samedi: Universal API

Samedi Booking API wrapper for appointment availability, patient information, and booking workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/samedi/latest
- **Category:** Productivity / Scheduling
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.samedi.com/
- **Vendor API docs:** https://api-docs.samedi.de/booking-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Health Insurances](actions/list-health-insurances.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samedi/latest/actions/list-health-insurances?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Appointment Booking

| Action | Method | Description |
| --- | --- | --- |
| [Book Appointment](actions/book-appointment.md) | POST | Books an appointment in Samedi. |

### Appointment Category

| Action | Method | Description |
| --- | --- | --- |
| [List Appointment Categories](actions/list-appointment-categories.md) | GET | Retrieves appointment categories from Samedi. |

### Appointment Type

| Action | Method | Description |
| --- | --- | --- |
| [List Appointment Types](actions/list-appointment-types.md) | GET | Retrieves appointment types from Samedi. |

### Available Day

| Action | Method | Description |
| --- | --- | --- |
| [List Available Days](actions/list-available-days.md) | GET | Retrieves available appointment days from Samedi. |

### Available Time

| Action | Method | Description |
| --- | --- | --- |
| [List Available Times](actions/list-available-times.md) | GET | Retrieves available appointment times from Samedi. |

### Guest Appointment Booking

| Action | Method | Description |
| --- | --- | --- |
| [Guest Book Appointment](actions/guest-book-appointment.md) | POST | Books an appointment in Samedi for a guest. |

### Guest Paid Appointment Booking

| Action | Method | Description |
| --- | --- | --- |
| [Guest Complete Paid Appointment](actions/guest-complete-paid-appointment.md) | POST | Completes a paid appointment booking in Samedi for a guest. |

### Health Insurance

| Action | Method | Description |
| --- | --- | --- |
| [List Health Insurances](actions/list-health-insurances.md) | GET | Retrieves health insurances from Samedi. |

### Institution

| Action | Method | Description |
| --- | --- | --- |
| [Get Institution Details](actions/get-institution-details.md) | GET | Retrieves institution details from Samedi. |

### Paid Appointment Booking

| Action | Method | Description |
| --- | --- | --- |
| [Complete Paid Appointment](actions/complete-paid-appointment.md) | POST | Completes a paid appointment booking in Samedi. |

### Patient Appointment

| Action | Method | Description |
| --- | --- | --- |
| [List Upcoming Patient Appointments](actions/list-upcoming-patient-appointments.md) | GET | Retrieves upcoming patient appointments from Samedi. |

### Patient User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Patient User](actions/get-current-patient-user.md) | GET | Retrieves the current patient user from Samedi. |

### Paypal Order

| Action | Method | Description |
| --- | --- | --- |
| [Create PayPal Order](actions/create-paypal-order.md) | POST | Creates a PayPal order in Samedi. |

