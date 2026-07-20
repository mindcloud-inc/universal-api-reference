# <img src="https://images.mindcloud.co/apps/icons/intake-q_1775831146139.png" alt="IntakeQ logo" width="28" height="28"> IntakeQ: Universal API

Access IntakeQ tenant data for questionnaires, clients, appointments, notes, invoices, claims, and files through the official IntakeQ REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/intakeQ/latest
- **Actions:** 45
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://intakeq.com
- **Vendor API docs:** https://support.intakeq.com/category/560-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download File](actions/download-file.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/download-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (45)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create Intake Form Authentication Token](actions/create-intake-form-authentication-token.md) | POST | Creates an intake form token in IntakeQ. |

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Appointment](actions/cancel-appointment.md) | DELETE | Cancels an appointment in IntakeQ. |
| [Create Appointment](actions/create-appointment.md) | POST | Creates a new appointment in IntakeQ. |
| [Get Appointment](actions/get-appointment.md) | GET | Retrieves an appointment from IntakeQ. |
| [Query Appointments](actions/query-appointments.md) | GET | Retrieves appointments from IntakeQ. |
| [Update Appointment](actions/update-appointment.md) | PUT | Updates an existing appointment in IntakeQ. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Query Claims](actions/query-claims.md) | GET | Retrieves claims from IntakeQ. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in IntakeQ. |
| [Query Clients](actions/query-clients.md) | GET | Retrieves clients from IntakeQ. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in IntakeQ. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Create Assistant](actions/create-assistant.md) | POST | Creates a new assistant in IntakeQ. |
| [Create Practitioner](actions/create-practitioner.md) | POST | Creates a new practitioner in IntakeQ. |
| [Delete Assistant](actions/delete-assistant.md) | DELETE | Deletes an assistant from IntakeQ. |
| [Delete Practitioner](actions/delete-practitioner.md) | DELETE | Deletes a practitioner from IntakeQ. |
| [Disable Practitioner](actions/disable-practitioner.md) | PUT | Disables a practitioner in IntakeQ. |
| [Enable Practitioner](actions/enable-practitioner.md) | PUT | Enables a practitioner in IntakeQ. |
| [List Assistants](actions/list-assistants.md) | GET | Retrieves assistants from IntakeQ. |
| [List Practitioners](actions/list-practitioners.md) | GET | Retrieves practitioners from IntakeQ. |
| [Transfer Client Ownership](actions/transfer-client-ownership.md) | PUT | Transfers client ownership in IntakeQ. |
| [Transfer Practitioner Data](actions/transfer-practitioner-data.md) | PUT | Transfers practitioner data in IntakeQ. |
| [Update Assistant](actions/update-assistant.md) | PUT | Updates an existing assistant in IntakeQ. |
| [Update Practitioner](actions/update-practitioner.md) | PUT | Updates an existing practitioner in IntakeQ. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from IntakeQ. |
| [Download File](actions/download-file.md) | GET | Retrieves a file from IntakeQ. |
| [List Client Files](actions/list-client-files.md) | GET | Retrieves client files from IntakeQ. |
| [Upload File](actions/upload-file.md) | POST | Creates a new client file in IntakeQ. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from IntakeQ. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Create Intake Form Link](actions/create-intake-form-link.md) | POST | Creates an intake form link in IntakeQ. |
| [Download Intake Consent PDF](actions/download-intake-consent-pdf.md) | GET | Retrieves an intake consent PDF from IntakeQ. |
| [Download Intake Form PDF](actions/download-intake-form-pdf.md) | GET | Retrieves an intake form PDF from IntakeQ. |
| [Get Intake Form](actions/get-intake-form.md) | GET | Retrieves an intake form from IntakeQ. |
| [Query Intake Forms](actions/query-intake-forms.md) | GET | Retrieves intake forms from IntakeQ. |
| [Resend Questionnaire](actions/resend-questionnaire.md) | PUT | Resends a questionnaire from IntakeQ. |
| [Send Questionnaire](actions/send-questionnaire.md) | POST | Creates a questionnaire request in IntakeQ. |
| [Update Office Use Questions](actions/update-office-use-questions.md) | PUT | Updates office-use intake answers in IntakeQ. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Questionnaire Templates](actions/list-questionnaire-templates.md) | GET | Retrieves questionnaire templates from IntakeQ. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from IntakeQ. |
| [Query Invoices](actions/query-invoices.md) | GET | Retrieves invoices from IntakeQ. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Download Treatment Note PDF](actions/download-treatment-note-pdf.md) | GET | Retrieves a treatment note PDF from IntakeQ. |
| [Get Client Diagnoses](actions/get-client-diagnoses.md) | GET | Retrieves client diagnoses from IntakeQ. |
| [Get Treatment Note](actions/get-treatment-note.md) | GET | Retrieves a treatment note from IntakeQ. |
| [Query Treatment Notes](actions/query-treatment-notes.md) | GET | Retrieves treatment notes from IntakeQ. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking Settings](actions/get-booking-settings.md) | GET | Retrieves booking settings from IntakeQ. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Add Client Tag](actions/add-client-tag.md) | POST | Creates a client tag assignment in IntakeQ. |
| [Remove Client Tag](actions/remove-client-tag.md) | DELETE | Deletes a client tag assignment from IntakeQ. |

