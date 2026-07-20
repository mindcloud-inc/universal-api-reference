# <img src="https://images.mindcloud.co/apps/icons/cerbo_1774367503596.png" alt="Cerbo logo" width="28" height="28"> Cerbo: Universal API

Cerbo provides all-in-one EHR and practice management software for modern healthcare practices.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cerbo/latest
- **Actions:** 127
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cer.bo/
- **Vendor API docs:** https://docs.cer.bo/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (127)

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | POST | Creates a new appointment in Cerbo. |
| [Delete Appointment](actions/delete-appointment.md) | DELETE | Deletes an existing appointment from Cerbo. |
| [Get Appointment](actions/get-appointment.md) | GET | Retrieves appointment details from Cerbo. |
| [List Appointments](actions/list-appointments.md) | GET | Retrieves appointment records from Cerbo. |
| [Update Appointment](actions/update-appointment.md) | PUT | Updates an existing appointment in Cerbo. |

### Appointment Availability

| Action | Method | Description |
| --- | --- | --- |
| [Get Appointment Availability](actions/get-appointment-availability.md) | GET | Retrieves appointment availability from Cerbo. |

### Appointment Reminder

| Action | Method | Description |
| --- | --- | --- |
| [List Appointment Reminders](actions/list-appointment-reminders.md) | GET | Retrieves appointment reminders from Cerbo. |

### Appointment Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment Type](actions/create-appointment-type.md) | POST | Creates a new appointment type in Cerbo. |
| [List Appointment Types](actions/list-appointment-types.md) | GET | Retrieves appointment types from Cerbo. |

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [Get Charge Definition](actions/get-charge-definition.md) | GET | Retrieves charge definition details from Cerbo. |
| [List Charge Definitions](actions/list-charge-definitions.md) | GET | Retrieves charge definitions from Cerbo. |
| [List System-Wide Charges](actions/list-system-wide-charges.md) | GET | Retrieves system-wide charges from Cerbo. |

### Charge By Id

| Action | Method | Description |
| --- | --- | --- |
| [Get Charge By ID](actions/get-charge-by-id.md) | GET | Retrieves charge details from Cerbo. |

### Delta

| Action | Method | Description |
| --- | --- | --- |
| [List Deltas](actions/list-deltas.md) | GET | Retrieves Cerbo delta changes for a resource type. |

### Drug

| Action | Method | Description |
| --- | --- | --- |
| [Get Drug](actions/get-drug.md) | GET | Retrieves drug details from Cerbo. |
| [Search Drugs](actions/search-drugs.md) | GET | Finds drugs in Cerbo by search term. |

### Drug Frequency

| Action | Method | Description |
| --- | --- | --- |
| [List Drug Frequencies](actions/list-drug-frequencies.md) | GET | Retrieves drug frequency definitions from Cerbo. |

### Email Appointment Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Appointment Reminder](actions/create-email-appointment-reminder.md) | POST | Creates a new email appointment reminder in Cerbo. |

### Encounter

| Action | Method | Description |
| --- | --- | --- |
| [Create Encounter](actions/create-encounter.md) | POST | Creates a new encounter in Cerbo. |
| [Delete Encounter](actions/delete-encounter.md) | DELETE | Deletes an existing encounter from Cerbo. |
| [Get Encounter](actions/get-encounter.md) | GET | Retrieves encounter details from Cerbo. |
| [List Encounters](actions/list-encounters.md) | GET | Retrieves patient encounters from Cerbo. |

### Encounter Charge

| Action | Method | Description |
| --- | --- | --- |
| [List Encounter Charges](actions/list-encounter-charges.md) | GET | Retrieves encounter charges from Cerbo. |

### Encounter Estimate

| Action | Method | Description |
| --- | --- | --- |
| [List Encounter Estimates](actions/list-encounter-estimates.md) | GET | Retrieves encounter estimates from Cerbo. |

### Encounter Type

| Action | Method | Description |
| --- | --- | --- |
| [List Encounter Types](actions/list-encounter-types.md) | GET | Retrieves encounter types from Cerbo. |

### Extended Patient Detail

| Action | Method | Description |
| --- | --- | --- |
| [List Extended Patient Details](actions/list-extended-patient-details.md) | GET | Retrieves extended patient details from Cerbo. |

### Facility

| Action | Method | Description |
| --- | --- | --- |
| [List Laboratory Definitions](actions/list-laboratory-definitions.md) | GET | Retrieves laboratory definitions from Cerbo. |

### Health Maintenance

| Action | Method | Description |
| --- | --- | --- |
| [Get Health Maintenance Tracker](actions/get-health-maintenance-tracker.md) | GET | Retrieves health maintenance tracker details from Cerbo. |
| [List Health Maintenance Trackers](actions/list-health-maintenance-trackers.md) | GET | Retrieves health maintenance trackers from Cerbo. |

### Inventory

| Action | Method | Description |
| --- | --- | --- |
| [Create Inventory](actions/create-inventory.md) | POST | Creates a new inventory item in Cerbo. |
| [Get Inventory](actions/get-inventory.md) | GET | Retrieves inventory item details from Cerbo. |
| [List Inventory](actions/list-inventory.md) | GET | Retrieves inventory records from Cerbo. |
| [Update Inventory](actions/update-inventory.md) | PUT | Updates an existing inventory item in Cerbo. |

### Partner App Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Partner App Order](actions/get-partner-app-order.md) | GET | Retrieves Quest order details from Cerbo. |
| [List Partner App Orders](actions/list-partner-app-orders.md) | GET | Retrieves Quest order records from Cerbo. |

### Partner App Order Raw

| Action | Method | Description |
| --- | --- | --- |
| [Get Partner App Order Raw](actions/get-partner-app-order-raw.md) | GET | Retrieves the raw Quest requisition document from Cerbo. |

### Patient

| Action | Method | Description |
| --- | --- | --- |
| [Create Patient](actions/create-patient.md) | POST | Creates a new patient in Cerbo. |
| [Delete Patient](actions/delete-patient.md) | DELETE | Deletes an existing patient from Cerbo. |
| [Get Patient](actions/get-patient.md) | GET | Retrieves patient details from Cerbo. |
| [List Patients](actions/list-patients.md) | GET | Retrieves patient records from Cerbo. |
| [Search Patients](actions/search-patients.md) | GET | Finds patients in Cerbo by search criteria. |
| [Update Patient](actions/update-patient.md) | PUT | Updates an existing patient in Cerbo. |

### Patient Blood Pressure Vital

| Action | Method | Description |
| --- | --- | --- |
| [Create Patient Blood Pressure Vital](actions/create-patient-blood-pressure-vital.md) | POST | Creates a new patient blood pressure vital in Cerbo. |
| [List Patient Blood Pressure Vitals](actions/list-patient-blood-pressure-vitals.md) | GET | Retrieves patient blood pressure vitals from Cerbo. |

### Patient Charge

| Action | Method | Description |
| --- | --- | --- |
| [List Patient Charges](actions/list-patient-charges.md) | GET | Retrieves patient charges from Cerbo. |

### Patient Custom Vital

| Action | Method | Description |
| --- | --- | --- |
| [Create Patient Custom Vital](actions/create-patient-custom-vital.md) | POST | Creates a new patient custom vital in Cerbo. |
| [List Patient Custom Vitals](actions/list-patient-custom-vitals.md) | GET | Retrieves patient custom vitals from Cerbo. |

### Patient Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Patient Document](actions/create-patient-document.md) | POST | Creates a new patient document in Cerbo. |
| [Get Patient Document](actions/get-patient-document.md) | GET | Retrieves patient document details from Cerbo. |
| [List Patient Documents](actions/list-patient-documents.md) | GET | Retrieves patient documents from Cerbo. |
| [Stream Patient Document](actions/stream-patient-document.md) | GET | Streams patient document content from Cerbo. |

### Patient Document Raw

| Action | Method | Description |
| --- | --- | --- |
| [Get Patient Document Raw](actions/get-patient-document-raw.md) | GET | Retrieves raw patient document content from Cerbo. |

### Patient Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Patient Email](actions/send-patient-email.md) | PUT | Sends an email to a Cerbo patient. |

### Patient Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Get Patient Estimate](actions/get-patient-estimate.md) | GET | Retrieves patient estimate details from Cerbo. |
| [List Patient Estimates](actions/list-patient-estimates.md) | GET | Retrieves patient estimates from Cerbo. |

### Patient Facility

| Action | Method | Description |
| --- | --- | --- |
| [Add Patient Laboratory](actions/add-patient-laboratory.md) | POST | Adds a patient laboratory record in Cerbo. |
| [Delete Patient Laboratory](actions/delete-patient-laboratory.md) | DELETE | Deletes a patient laboratory from Cerbo. |
| [List Patient Laboratories](actions/list-patient-laboratories.md) | GET | Retrieves patient laboratories from Cerbo. |

### Patient Health Maintenance

| Action | Method | Description |
| --- | --- | --- |
| [Add Patient Health Maintenance Reading](actions/add-patient-health-maintenance-reading.md) | POST | Adds a patient health maintenance reading in Cerbo. |
| [List Patient Health Maintenance Readings](actions/list-patient-health-maintenance-readings.md) | GET | Retrieves patient health maintenance readings from Cerbo. |

### Patient Height Vital

| Action | Method | Description |
| --- | --- | --- |
| [Create Patient Height Vital](actions/create-patient-height-vital.md) | POST | Creates a new patient height vital in Cerbo. |
| [List Patient Height Vitals](actions/list-patient-height-vitals.md) | GET | Retrieves patient height vitals from Cerbo. |

### Patient Image

| Action | Method | Description |
| --- | --- | --- |
| [Create Patient Image](actions/create-patient-image.md) | POST | Creates a new patient image in Cerbo. |
| [Get Patient Image](actions/get-patient-image.md) | GET | Retrieves patient image details from Cerbo. |
| [List Patient Images](actions/list-patient-images.md) | GET | Retrieves patient images from Cerbo. |
| [Stream Patient Image](actions/stream-patient-image.md) | GET | Streams patient image content from Cerbo. |

### Patient Image Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Patient Image Content](actions/get-patient-image-content.md) | GET | Retrieves raw patient image content from Cerbo. |

### Patient Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Patient Invoice](actions/get-patient-invoice.md) | GET | Retrieves patient invoice details from Cerbo. |
| [List Patient Invoices](actions/list-patient-invoices.md) | GET | Retrieves patient invoices from Cerbo. |

### Patient Lab Result

| Action | Method | Description |
| --- | --- | --- |
| [List Patient Lab Results](actions/list-patient-lab-results.md) | GET | Retrieves patient lab results from Cerbo. |

### Patient Note

| Action | Method | Description |
| --- | --- | --- |
| [List Patient Free-Text Notes](actions/list-patient-free-text-notes.md) | GET | Retrieves patient free-text notes from Cerbo. |
| [List Patient Free-Text Notes by Type](actions/list-patient-free-text-notes-by-type.md) | GET | Retrieves patient free-text notes by type from Cerbo. |
| [List Patient Note Types](actions/list-patient-note-types.md) | GET | Retrieves patient note types from Cerbo. |
| [Update Patient Note](actions/update-patient-note.md) | PUT | Updates a patient free-text note in Cerbo. |

### Patient Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Patient Order](actions/get-patient-order.md) | GET | Retrieves patient order details from Cerbo. |
| [List Patient Orders](actions/list-patient-orders.md) | GET | Retrieves patient orders from Cerbo. |

### Patient Past Medical History

| Action | Method | Description |
| --- | --- | --- |
| [List Patient Past Medical History](actions/list-patient-past-medical-history.md) | GET | Retrieves patient past medical history from Cerbo. |

### Patient Pharmacy

| Action | Method | Description |
| --- | --- | --- |
| [List Patient Pharmacies](actions/list-patient-pharmacies.md) | GET | Retrieves patient pharmacies from Cerbo. |

### Patient Prescription

| Action | Method | Description |
| --- | --- | --- |
| [Discontinue Patient Prescription](actions/discontinue-patient-prescription.md) | PUT | Discontinues an existing patient prescription in Cerbo. |
| [Get Patient Prescription](actions/get-patient-prescription.md) | GET | Retrieves patient prescription details from Cerbo. |
| [List Patient Prescriptions](actions/list-patient-prescriptions.md) | GET | Retrieves patient prescriptions from Cerbo. |
| [Queue Patient Prescription](actions/queue-patient-prescription.md) | POST | Queues a patient prescription request in Cerbo. |
| [Refill Patient Prescription](actions/refill-patient-prescription.md) | PUT | Queues a patient prescription refill in Cerbo. |

### Patient Questionnaire

| Action | Method | Description |
| --- | --- | --- |
| [Create Patient Questionnaire](actions/create-patient-questionnaire.md) | POST | Creates a new patient questionnaire in Cerbo. |
| [Get Patient Questionnaire](actions/get-patient-questionnaire.md) | GET | Retrieves patient questionnaire details from Cerbo. |
| [List Patient Questionnaires](actions/list-patient-questionnaires.md) | GET | Retrieves patient questionnaires from Cerbo. |

### Patient Specialist

| Action | Method | Description |
| --- | --- | --- |
| [Create Patient Specialist](actions/create-patient-specialist.md) | POST | Creates a patient specialist record in Cerbo. |
| [Delete Patient Specialist](actions/delete-patient-specialist.md) | DELETE | Deletes a patient specialist from Cerbo. |
| [List Patient Specialists](actions/list-patient-specialists.md) | GET | Retrieves patient specialists from Cerbo. |

### Patient Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Patient Subscriptions](actions/list-patient-subscriptions.md) | GET | Retrieves patient subscriptions from Cerbo. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscription records from Cerbo. |

### Patient Supplement

| Action | Method | Description |
| --- | --- | --- |
| [Discontinue Patient Supplement](actions/discontinue-patient-supplement.md) | PUT | Discontinues an existing patient supplement in Cerbo. |
| [Get Patient Supplement](actions/get-patient-supplement.md) | GET | Retrieves patient supplement details from Cerbo. |
| [List Patient Supplements](actions/list-patient-supplements.md) | GET | Retrieves patient supplements from Cerbo. |
| [Queue Patient Supplement](actions/queue-patient-supplement.md) | POST | Queues a patient supplement request in Cerbo. |

### Patient Tag

| Action | Method | Description |
| --- | --- | --- |
| [Delete Patient Tag](actions/delete-patient-tag.md) | DELETE | Deletes a patient tag from Cerbo. |
| [List Patient Tags](actions/list-patient-tags.md) | GET | Retrieves patient tags from Cerbo. |
| [Update Patient Tags](actions/update-patient-tags.md) | PUT | Updates patient tags in Cerbo. |

### Patient Vaccine

| Action | Method | Description |
| --- | --- | --- |
| [List Patient Vaccines](actions/list-patient-vaccines.md) | GET | Retrieves patient vaccines from Cerbo. |

### Patient Weight Vital

| Action | Method | Description |
| --- | --- | --- |
| [Create Patient Weight Vital](actions/create-patient-weight-vital.md) | POST | Creates a new patient weight vital in Cerbo. |
| [List Patient Weight Vitals](actions/list-patient-weight-vitals.md) | GET | Retrieves patient weight vitals from Cerbo. |

### Portal Credential

| Action | Method | Description |
| --- | --- | --- |
| [Validate Portal Credentials](actions/validate-portal-credentials.md) | GET | Validates Cerbo patient portal login credentials. |

### Portal Request

| Action | Method | Description |
| --- | --- | --- |
| [Delete Portal Request](actions/delete-portal-request.md) | DELETE | Deletes a queued patient portal request from Cerbo. |
| [List Portal Requests](actions/list-portal-requests.md) | GET | Retrieves queued patient portal requests from Cerbo. |

### Secure Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Secure Message](actions/create-secure-message.md) | POST | Creates a secure patient message in Cerbo. |
| [List Secure Messages](actions/list-secure-messages.md) | GET | Retrieves secure patient messages from Cerbo. |

### Sms Appointment Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Create SMS Appointment Reminder](actions/create-sms-appointment-reminder.md) | POST | Creates a new SMS appointment reminder in Cerbo. |

### Supplement

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplement](actions/create-supplement.md) | POST | Creates a new supplement in Cerbo. |
| [Get Supplement](actions/get-supplement.md) | GET | Retrieves supplement details from Cerbo. |
| [List Supplements](actions/list-supplements.md) | GET | Retrieves supplement records from Cerbo. |
| [Search Supplements](actions/search-supplements.md) | GET | Finds supplements in Cerbo by search terms. |
| [Update Supplement](actions/update-supplement.md) | PUT | Updates an existing supplement in Cerbo. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Cerbo. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Cerbo. |
| [List Tag Definitions](actions/list-tag-definitions.md) | GET | Retrieves tag definitions from Cerbo. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Cerbo. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Cerbo. |
| [Get Task](actions/get-task.md) | GET | Retrieves task details from Cerbo. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves task records from Cerbo. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Cerbo. |

### To Portal

| Action | Method | Description |
| --- | --- | --- |
| [Invite To Portal](actions/invite-to-portal.md) | PUT | Sends a Cerbo patient portal invitation email. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves user details from Cerbo. |
| [List Users](actions/list-users.md) | GET | Retrieves user records from Cerbo. |

### User Credential

| Action | Method | Description |
| --- | --- | --- |
| [Validate User Credentials](actions/validate-user-credentials.md) | GET | Validates Cerbo user login credentials. |

### Vital

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Vital Definition](actions/get-custom-vital-definition.md) | GET | Retrieves custom vital definition details from Cerbo. |
| [List Custom Vital Definitions](actions/list-custom-vital-definitions.md) | GET | Retrieves custom vital definitions from Cerbo. |

### Vitals Tag Group

| Action | Method | Description |
| --- | --- | --- |
| [List Vitals Tag Groups](actions/list-vitals-tag-groups.md) | GET | Retrieves vitals tag groups from Cerbo. |

