# <img src="https://images.mindcloud.co/apps/icons/cliniko_1775854217630.png" alt="Cliniko logo" width="28" height="28"> Cliniko: Universal API

Manage patients, appointments, invoices, and treatment notes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cliniko/latest
- **Category:** Productivity / Scheduling
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cliniko.com/
- **Vendor API docs:** https://docs.api.cliniko.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Patients](actions/list-patients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-patients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Appointment Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Appointment Type](actions/get-appointment-type.md) | GET | Retrieves an appointment type from your Cliniko account. |
| [List Appointment Types](actions/list-appointment-types.md) | GET | Retrieves appointment types from your Cliniko account. |

### Attendee

| Action | Method | Description |
| --- | --- | --- |
| [Get Attendee](actions/get-attendee.md) | GET | Retrieves an attendee from your Cliniko account. |
| [List Attendees](actions/list-attendees.md) | GET | Retrieves attendees from your Cliniko account. |

### Billable Item

| Action | Method | Description |
| --- | --- | --- |
| [List Billable Items](actions/list-billable-items.md) | GET | Retrieves billable items from your Cliniko account. |

### Business

| Action | Method | Description |
| --- | --- | --- |
| [Get Business](actions/get-business.md) | GET | Retrieves a business from your Cliniko account. |
| [List Businesses](actions/list-businesses.md) | GET | Retrieves businesses from your Cliniko account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your Cliniko account. |

### Group Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Appointment](actions/get-group-appointment.md) | GET | Retrieves a group appointment from your Cliniko account. |
| [List Group Appointments](actions/list-group-appointments.md) | GET | Retrieves group appointments from your Cliniko account. |

### Individual Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Get Individual Appointment](actions/get-individual-appointment.md) | GET | Retrieves an individual appointment from your Cliniko account. |
| [List Individual Appointments](actions/list-individual-appointments.md) | GET | Retrieves individual appointments from your Cliniko account. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from your Cliniko account. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from your Cliniko account. |

### Invoice Item

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Items](actions/list-invoice-items.md) | GET | Retrieves invoice items from your Cliniko account. |

### Medical Alert

| Action | Method | Description |
| --- | --- | --- |
| [List Medical Alerts](actions/list-medical-alerts.md) | GET | Retrieves medical alerts from your Cliniko account. |

### Patient

| Action | Method | Description |
| --- | --- | --- |
| [Get Patient](actions/get-patient.md) | GET | Retrieves a patient record from your Cliniko account. |
| [List Patients](actions/list-patients.md) | GET | Retrieves patient records from your Cliniko account. |

### Patient Case

| Action | Method | Description |
| --- | --- | --- |
| [Get Patient Case](actions/get-patient-case.md) | GET | Retrieves a patient case from your Cliniko account. |
| [List Patient Cases](actions/list-patient-cases.md) | GET | Retrieves patient cases from your Cliniko account. |

### Practitioner

| Action | Method | Description |
| --- | --- | --- |
| [Get Practitioner](actions/get-practitioner.md) | GET | Retrieves a practitioner from your Cliniko account. |
| [List Practitioners](actions/list-practitioners.md) | GET | Retrieves practitioners from your Cliniko account. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from your Cliniko account. |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Settings](actions/get-settings.md) | GET | Retrieves settings from your Cliniko account. |

