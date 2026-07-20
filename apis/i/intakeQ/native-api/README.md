# IntakeQ: Native API Reference

A consolidated summary of IntakeQ's API configuration and 45 documented operations, with links to official documentation.

- **Official docs:** https://support.intakeq.com/category/560-api
- **API base URL:** `https://intakeq.com/api/v1`

## Authentication

### API Key

Provide your IntakeQ Developer API key. Runtime requests send it in the X-Auth-Key header exactly as required by IntakeQ.

### Credentials

- **API Key:** `apiKey` · required · Your IntakeQ Developer API key from More > Settings > Integrations > Developer API. MindCloud sends it in the X-Auth-Key header.

Send these headers with each API request:

```http
X-Auth-Key: <apiKey>
```

[Official authentication documentation](https://support.intakeq.com/category/560-api)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (45 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Client Tag](actions/add-client-tag.md) | `POST /clientTags` | [docs](https://support.intakeq.com/article/251-intakeq-client-api) |
| [Cancel Appointment](actions/cancel-appointment.md) | `POST /appointments/cancellation` | [docs](https://support.intakeq.com/article/204-intakeq-appointments-api) |
| [Create Appointment](actions/create-appointment.md) | `POST /appointments` | [docs](https://support.intakeq.com/article/204-intakeq-appointments-api) |
| [Create Assistant](actions/create-assistant.md) | `POST /assistants` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://support.intakeq.com/article/251-intakeq-client-api) |
| [Create Intake Form Authentication Token](actions/create-intake-form-authentication-token.md) | `POST /intakes/{id}/token` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [Create Intake Form Link](actions/create-intake-form-link.md) | `POST /intakes/create` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [Create Practitioner](actions/create-practitioner.md) | `POST /practitioners` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [Delete Assistant](actions/delete-assistant.md) | `DELETE /assistants/{assistantId}` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [Delete File](actions/delete-file.md) | `DELETE /files/{fileId}` | [docs](https://support.intakeq.com/article/430-intakeq-files-api) |
| [Delete Practitioner](actions/delete-practitioner.md) | `DELETE /practitioners/{practitionerId}` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [Disable Practitioner](actions/disable-practitioner.md) | `POST /practitioners/{practitionerId}/disable` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [Download File](actions/download-file.md) | `GET /files/{fileId}` | [docs](https://support.intakeq.com/article/430-intakeq-files-api) |
| [Download Intake Consent PDF](actions/download-intake-consent-pdf.md) | `GET /intakes/{intakeId}/consent/{consentFormId}/pdf` | [docs](https://support.intakeq.com/article/31-intakeq-api) |
| [Download Intake Form PDF](actions/download-intake-form-pdf.md) | `GET /intakes/{intakeId}/pdf` | [docs](https://support.intakeq.com/article/31-intakeq-api) |
| [Download Treatment Note PDF](actions/download-treatment-note-pdf.md) | `GET /notes/{noteId}/pdf` | [docs](https://support.intakeq.com/article/342-intakeq-notes-api) |
| [Enable Practitioner](actions/enable-practitioner.md) | `POST /practitioners/{practitionerId}/enable` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [Get Appointment](actions/get-appointment.md) | `GET /appointments/{appointmentId}` | [docs](https://support.intakeq.com/article/204-intakeq-appointments-api) |
| [Get Booking Settings](actions/get-booking-settings.md) | `GET /appointments/settings` | [docs](https://support.intakeq.com/article/204-intakeq-appointments-api) |
| [Get Client Diagnoses](actions/get-client-diagnoses.md) | `GET /client/{clientId}/diagnoses` | [docs](https://support.intakeq.com/article/251-intakeq-client-api) |
| [Get Intake Form](actions/get-intake-form.md) | `GET /intakes/{intakeId}` | [docs](https://support.intakeq.com/article/31-intakeq-api) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/{invoiceId}` | [docs](https://support.intakeq.com/article/385-intakeq-invoice-api) |
| [Get Treatment Note](actions/get-treatment-note.md) | `GET /notes/{noteId}` | [docs](https://support.intakeq.com/article/342-intakeq-notes-api) |
| [List Assistants](actions/list-assistants.md) | `GET /assistants` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [List Client Files](actions/list-client-files.md) | `GET /files` | [docs](https://support.intakeq.com/article/430-intakeq-files-api) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://support.intakeq.com/article/430-intakeq-files-api) |
| [List Practitioners](actions/list-practitioners.md) | `GET /practitioners` | [docs](https://support.intakeq.com/article/31-intakeq-api) |
| [List Questionnaire Templates](actions/list-questionnaire-templates.md) | `GET /questionnaires` | [docs](https://support.intakeq.com/article/31-intakeq-api) |
| [Query Appointments](actions/query-appointments.md) | `GET /appointments` | [docs](https://support.intakeq.com/article/204-intakeq-appointments-api) |
| [Query Claims](actions/query-claims.md) | `GET /claims` | [docs](https://support.intakeq.com/article/568-intakeq-claims-api) |
| [Query Clients](actions/query-clients.md) | `GET /clients` | [docs](https://support.intakeq.com/article/251-intakeq-client-api) |
| [Query Intake Forms](actions/query-intake-forms.md) | `GET /intakes/summary` | [docs](https://support.intakeq.com/article/31-intakeq-api) |
| [Query Invoices](actions/query-invoices.md) | `GET /invoices` | [docs](https://support.intakeq.com/article/385-intakeq-invoice-api) |
| [Query Treatment Notes](actions/query-treatment-notes.md) | `GET /notes/summary` | [docs](https://support.intakeq.com/article/342-intakeq-notes-api) |
| [Remove Client Tag](actions/remove-client-tag.md) | `DELETE /clientTags` | [docs](https://support.intakeq.com/article/251-intakeq-client-api) |
| [Resend Questionnaire](actions/resend-questionnaire.md) | `POST /intakes/resend` | [docs](https://support.intakeq.com/article/31-intakeq-api) |
| [Send Questionnaire](actions/send-questionnaire.md) | `POST /intakes/send` | [docs](https://support.intakeq.com/article/31-intakeq-api) |
| [Transfer Client Ownership](actions/transfer-client-ownership.md) | `POST /practitioners/{sourcePractitionerId}/transferClientOwnership/{destinationPractitionerId}` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [Transfer Practitioner Data](actions/transfer-practitioner-data.md) | `POST /practitioners/{sourcePractitionerId}/transferData/{destinationPractitionerId}` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [Update Appointment](actions/update-appointment.md) | `PUT /appointments` | [docs](https://support.intakeq.com/article/204-intakeq-appointments-api) |
| [Update Assistant](actions/update-assistant.md) | `PUT /assistants` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [Update Client](actions/update-client.md) | `POST /clients` | [docs](https://support.intakeq.com/article/251-intakeq-client-api) |
| [Update Office Use Questions](actions/update-office-use-questions.md) | `POST /intakes` | [docs](https://support.intakeq.com/article/31-intakeq-api) |
| [Update Practitioner](actions/update-practitioner.md) | `PUT /practitioners` | [docs](https://support.intakeq.com/article/433-intakeq-partner-api) |
| [Upload File](actions/upload-file.md) | `POST /files/{clientId}` | [docs](https://support.intakeq.com/article/430-intakeq-files-api) |
