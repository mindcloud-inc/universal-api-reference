# Cerbo: Native API Reference

A consolidated summary of Cerbo's API configuration and 127 documented operations, with links to official documentation.

- **Official docs:** https://docs.cer.bo/
- **API base URL:** `https://{tenant}.md-hq.com/api/v1`

## Authentication

### Basic Auth

Connect to a Cerbo tenant using the API user, API secret, and tenant subdomain required by Cerbo's Basic-auth API.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Tenant Subdomain:** `tenant` · required · Cerbo tenant subdomain, for example your-practice from your-practice.md-hq.com.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.cer.bo/#section/Best-Practices/Security)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (127 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Patient Health Maintenance Reading](actions/add-patient-health-maintenance-reading.md) | `POST /patients/:patient_id/health_maintenance/:health_maintenance_id` | [docs](https://docs.cer.bo/#tag/Patient-Health-Maintenance/operation/createPatientHealthMaintenance) |
| [Add Patient Laboratory](actions/add-patient-laboratory.md) | `POST /patients/:patient_id/laboratories` | [docs](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/createPatientFacility) |
| [Create Appointment](actions/create-appointment.md) | `POST /appointments` | [docs](https://docs.cer.bo/#tag/Appointments/operation/createAppointment) |
| [Create Appointment Type](actions/create-appointment-type.md) | `POST /appointment_types` | [docs](https://docs.cer.bo/#tag/Appointment-Types/operation/createAppointmentType) |
| [Create Email Appointment Reminder](actions/create-email-appointment-reminder.md) | `POST /appointments/:appointment_id/reminders/email` | [docs](https://docs.cer.bo/#tag/Appointment-Reminders/operation/createEmailAppointmentReminder) |
| [Create Encounter](actions/create-encounter.md) | `POST /encounters` | [docs](https://docs.cer.bo/#tag/Encounters/operation/createEncounter) |
| [Create Inventory](actions/create-inventory.md) | `POST /inventory` | [docs](https://docs.cer.bo/#tag/Inventory/operation/createInventory) |
| [Create Patient](actions/create-patient.md) | `POST /patients` | [docs](https://docs.cer.bo/#tag/Patients/operation/createPatient) |
| [Create Patient Blood Pressure Vital](actions/create-patient-blood-pressure-vital.md) | `POST /patients/:patient_id/vitals/bp` | [docs](https://docs.cer.bo/#tag/Patient-Vitals/operation/createPatientBloodPressureVital) |
| [Create Patient Custom Vital](actions/create-patient-custom-vital.md) | `POST /patients/:patient_id/vitals/:vital_id` | [docs](https://docs.cer.bo/#tag/Patient-Vitals/operation/createPatientCustomVital) |
| [Create Patient Document](actions/create-patient-document.md) | `POST /patients/:patient_id/documents` | [docs](https://docs.cer.bo/#tag/Patient-Documents/operation/createPatientDocument) |
| [Create Patient Height Vital](actions/create-patient-height-vital.md) | `POST /patients/:patient_id/vitals/height` | [docs](https://docs.cer.bo/#tag/Patient-Vitals/operation/createPatientHeightVital) |
| [Create Patient Image](actions/create-patient-image.md) | `POST /patients/:patient_id/images` | [docs](https://docs.cer.bo/#tag/Patient-Images/operation/createPatientImage) |
| [Create Patient Questionnaire](actions/create-patient-questionnaire.md) | `POST /patients/:patient_id/questionnaires` | [docs](https://docs.cer.bo/#tag/Questionnaires/operation/createPatientQuestionnaire) |
| [Create Patient Specialist](actions/create-patient-specialist.md) | `POST /patients/:patient_id/specialists` | [docs](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/createPatientSpecialist) |
| [Create Patient Weight Vital](actions/create-patient-weight-vital.md) | `POST /patients/:patient_id/vitals/weight` | [docs](https://docs.cer.bo/#tag/Patient-Vitals/operation/createPatientWeightVital) |
| [Create Secure Message](actions/create-secure-message.md) | `POST /patients/:patient_id/portal/secure_messages` | [docs](https://docs.cer.bo/#tag/Secure-Messages/operation/createSecureMessage) |
| [Create SMS Appointment Reminder](actions/create-sms-appointment-reminder.md) | `POST /appointments/:appointment_id/reminders/sms` | [docs](https://docs.cer.bo/#tag/Appointment-Reminders/operation/createSmsAppointmentReminder) |
| [Create Supplement](actions/create-supplement.md) | `POST /supplements` | [docs](https://docs.cer.bo/#tag/Supplements/operation/createSupplement) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://docs.cer.bo/#tag/Tags/operation/createTag) |
| [Create Task](actions/create-task.md) | `POST /task` | [docs](https://docs.cer.bo/#tag/Tasks/operation/createTask) |
| [Delete Appointment](actions/delete-appointment.md) | `DELETE /appointments/:appointment_id` | [docs](https://docs.cer.bo/#tag/Appointments/operation/deleteAppointment) |
| [Delete Encounter](actions/delete-encounter.md) | `DELETE /encounters/:encounter_id` | [docs](https://docs.cer.bo/#tag/Encounters/operation/deleteEncounter) |
| [Delete Patient](actions/delete-patient.md) | `DELETE /patients/:patient_id` | [docs](https://docs.cer.bo/#tag/Patients/operation/deletePatient) |
| [Delete Patient Laboratory](actions/delete-patient-laboratory.md) | `DELETE /patients/:patient_id/laboratories/:patient_laboratory_id` | [docs](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/deletePatientFacility) |
| [Delete Patient Specialist](actions/delete-patient-specialist.md) | `DELETE /patients/:patient_id/specialists/:patient_specialist_id` | [docs](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/deletePatientSpecialist) |
| [Delete Patient Tag](actions/delete-patient-tag.md) | `DELETE /patients/:patient_id/tags/:tag_name` | [docs](https://docs.cer.bo/#tag/Patient-Tags/operation/deletePatientTag) |
| [Delete Portal Request](actions/delete-portal-request.md) | `DELETE /patients/:pt_id/portal/enqueued/:queue_request_id` | [docs](https://docs.cer.bo/#tag/Patient-Portal/operation/deletePortalRequest) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/:tag_id` | [docs](https://docs.cer.bo/#tag/Tags/operation/deleteTag) |
| [Discontinue Patient Prescription](actions/discontinue-patient-prescription.md) | `PATCH /patients/:pt_id/rxs/:pt_rx_id/discontinue` | [docs](https://docs.cer.bo/#tag/Patient-Prescriptions/operation/discontinuePatientPrescription) |
| [Discontinue Patient Supplement](actions/discontinue-patient-supplement.md) | `PATCH /patients/:pt_id/supplements/:pt_plan_other_id/discontinue` | [docs](https://docs.cer.bo/#tag/Patient-Supplements/operation/discontinuePatientSupplement) |
| [Get Appointment](actions/get-appointment.md) | `GET /appointments/:appointment_id` | [docs](https://docs.cer.bo/#tag/Appointments/operation/showAppointment) |
| [Get Appointment Availability](actions/get-appointment-availability.md) | `GET /appointments/availability` | [docs](https://docs.cer.bo/#tag/Appointment-Availability/operation/getAppointmentAvailability) |
| [Get Charge By ID](actions/get-charge-by-id.md) | `GET /charges/:charge_id` | [docs](https://docs.cer.bo/#tag/Charges/operation/showChargeById) |
| [Get Charge Definition](actions/get-charge-definition.md) | `GET /charge_master/:charge_id` | [docs](https://docs.cer.bo/#tag/Charges/operation/showCharge) |
| [Get Custom Vital Definition](actions/get-custom-vital-definition.md) | `GET /vitals/:vital_id` | [docs](https://docs.cer.bo/#tag/Vitals/operation/getVital) |
| [Get Drug](actions/get-drug.md) | `GET /drugs/:drug_id` | [docs](https://docs.cer.bo/#tag/Drugs/operation/showDrug) |
| [Get Encounter](actions/get-encounter.md) | `GET /encounters/:encounter_id` | [docs](https://docs.cer.bo/#tag/Encounters/operation/showEncounter) |
| [Get Health Maintenance Tracker](actions/get-health-maintenance-tracker.md) | `GET /health_maintenance/:health_maintenance_id` | [docs](https://docs.cer.bo/#tag/Health-Maintenance/operation/showHealthMaintenance) |
| [Get Inventory](actions/get-inventory.md) | `GET /inventory/:id` | [docs](https://docs.cer.bo/#tag/Inventory/operation/showInventory) |
| [Get Partner App Order](actions/get-partner-app-order.md) | `GET /partners/quest/orders/:order_id` | [docs](https://docs.cer.bo/#tag/Partner-Applications/operation/showPartnerAppOrder) |
| [Get Partner App Order Raw](actions/get-partner-app-order-raw.md) | `GET /partners/quest/requisition/:order_id/content` | [docs](https://docs.cer.bo/#tag/Partner-Applications/operation/showPartnerAppOrderRaw) |
| [Get Patient](actions/get-patient.md) | `GET /patients/:patient_id` | [docs](https://docs.cer.bo/#tag/Patients/operation/showPatient) |
| [Get Patient Document](actions/get-patient-document.md) | `GET /documents/:document_id` | [docs](https://docs.cer.bo/#tag/Patient-Documents/operation/showPatientDocument) |
| [Get Patient Document Raw](actions/get-patient-document-raw.md) | `GET /documents/:document_id/content` | [docs](https://docs.cer.bo/#tag/Patient-Documents/operation/showPatientDocumentRaw) |
| [Get Patient Estimate](actions/get-patient-estimate.md) | `GET /patients/:pt_id/estimates/:estimate_id` | [docs](https://docs.cer.bo/#tag/Patient-Charges/operation/showPatientEstimate) |
| [Get Patient Image](actions/get-patient-image.md) | `GET /patients/:patient_id/images/:image_id` | [docs](https://docs.cer.bo/#tag/Patient-Images/operation/showPatientImage) |
| [Get Patient Image Content](actions/get-patient-image-content.md) | `GET /patients/:patient_id/images/:image_id/content` | [docs](https://docs.cer.bo/#tag/Patient-Images/operation/showPatientImageContent) |
| [Get Patient Invoice](actions/get-patient-invoice.md) | `GET /invoices/:invoice_id` | [docs](https://docs.cer.bo/#tag/Patient-Invoices/operation/showPatientInvoice) |
| [Get Patient Order](actions/get-patient-order.md) | `GET /patients/:patient_id/orders/:order_id` | [docs](https://docs.cer.bo/#tag/Patient-Orders/operation/showPatientOrder) |
| [Get Patient Prescription](actions/get-patient-prescription.md) | `GET /patients/:patient_id/rxs/:medication_prescribed_id` | [docs](https://docs.cer.bo/#tag/Patient-Prescriptions/operation/showPatientPrescription) |
| [Get Patient Questionnaire](actions/get-patient-questionnaire.md) | `GET /patients/:patient_id/questionnaires/:questionnaire_id` | [docs](https://docs.cer.bo/#tag/Questionnaires/operation/showPatientQuestionnaire) |
| [Get Patient Supplement](actions/get-patient-supplement.md) | `GET /patients/:patient_id/supplements/:supplement_prescribed_id` | [docs](https://docs.cer.bo/#tag/Patient-Supplements/operation/showPatientSupplement) |
| [Get Supplement](actions/get-supplement.md) | `GET /supplements/:supplement_id` | [docs](https://docs.cer.bo/#tag/Supplements/operation/showSupplement) |
| [Get Task](actions/get-task.md) | `GET /task/:task_id` | [docs](https://docs.cer.bo/#tag/Tasks/operation/showTask) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://docs.cer.bo/#tag/Users/operation/showUser) |
| [Invite To Portal](actions/invite-to-portal.md) | `POST /patients/:pt_id/portal/invite` | [docs](https://docs.cer.bo/#tag/Patient-Portal/operation/inviteToPortal) |
| [List Appointment Reminders](actions/list-appointment-reminders.md) | `GET /appointments/:appointment_id/reminders` | [docs](https://docs.cer.bo/#tag/Appointment-Reminders/operation/listAppointmentReminders) |
| [List Appointment Types](actions/list-appointment-types.md) | `GET /appointment_types` | [docs](https://docs.cer.bo/#tag/Appointment-Types/operation/listAppointmentTypes) |
| [List Appointments](actions/list-appointments.md) | `GET /appointments` | [docs](https://docs.cer.bo/#tag/Appointments/operation/listAppointments) |
| [List Charge Definitions](actions/list-charge-definitions.md) | `GET /charge_master` | [docs](https://docs.cer.bo/#tag/Charges/operation/listCharges) |
| [List Custom Vital Definitions](actions/list-custom-vital-definitions.md) | `GET /vitals` | [docs](https://docs.cer.bo/#tag/Vitals/operation/getVitals) |
| [List Deltas](actions/list-deltas.md) | `GET /delta/:resource_type` | [docs](https://docs.cer.bo/#tag/Deltas/operation/listDeltas) |
| [List Drug Frequencies](actions/list-drug-frequencies.md) | `GET /drugs/frequencies` | [docs](https://docs.cer.bo/#tag/Drugs/operation/listDrugFrequencies) |
| [List Encounter Charges](actions/list-encounter-charges.md) | `GET /patients/:pt_id/encounters/:encounter_id/charges` | [docs](https://docs.cer.bo/#tag/Charges/operation/listEncounterCharges) |
| [List Encounter Estimates](actions/list-encounter-estimates.md) | `GET /patients/:pt_id/encounters/:encounter_id/estimates` | [docs](https://docs.cer.bo/#tag/Patient-Charges/operation/listEncounterEstimates) |
| [List Encounter Types](actions/list-encounter-types.md) | `GET /encounter_types` | [docs](https://docs.cer.bo/#tag/Encounter-Types/operation/listEncounterTypes) |
| [List Encounters](actions/list-encounters.md) | `GET /patients/:patient_id/encounters` | [docs](https://docs.cer.bo/#tag/Encounters/operation/listEncounters) |
| [List Extended Patient Details](actions/list-extended-patient-details.md) | `GET /patients/:id/extended_details` | [docs](https://docs.cer.bo/#tag/Extended-Patient-Details/operation/getExtendedPatientDetails) |
| [List Health Maintenance Trackers](actions/list-health-maintenance-trackers.md) | `GET /health_maintenance` | [docs](https://docs.cer.bo/#tag/Health-Maintenance/operation/listHealthMaintenance) |
| [List Inventory](actions/list-inventory.md) | `GET /inventory` | [docs](https://docs.cer.bo/#tag/Inventory/operation/listInventory) |
| [List Laboratory Definitions](actions/list-laboratory-definitions.md) | `GET /laboratories` | [docs](https://docs.cer.bo/#tag/Facilities/operation/listFacilities) |
| [List Partner App Orders](actions/list-partner-app-orders.md) | `GET /patients/:patient_id/partners/quest/orders` | [docs](https://docs.cer.bo/#tag/Partner-Applications/operation/listPartnerAppOrders) |
| [List Patient Blood Pressure Vitals](actions/list-patient-blood-pressure-vitals.md) | `GET /patients/:patient_id/vitals/bp` | [docs](https://docs.cer.bo/#tag/Patient-Vitals/operation/listPatientBloodPressureVitals) |
| [List Patient Charges](actions/list-patient-charges.md) | `GET /patients/:pt_id/charges` | [docs](https://docs.cer.bo/#tag/Charges/operation/listPatientCharges) |
| [List Patient Custom Vitals](actions/list-patient-custom-vitals.md) | `GET /patients/:patient_id/vitals/:vital_id` | [docs](https://docs.cer.bo/#tag/Patient-Vitals/operation/listPatientCustomVitals) |
| [List Patient Documents](actions/list-patient-documents.md) | `GET /patients/:patient_id/documents` | [docs](https://docs.cer.bo/#tag/Patient-Documents/operation/listPatientDocuments) |
| [List Patient Estimates](actions/list-patient-estimates.md) | `GET /patients/:pt_id/estimates` | [docs](https://docs.cer.bo/#tag/Patient-Charges/operation/listAllPatientEstimates) |
| [List Patient Free-Text Notes](actions/list-patient-free-text-notes.md) | `GET /patients/:patient_id/pt_notes` | [docs](https://docs.cer.bo/#tag/Patient-Free-Text-Notes/operation/listAllPatientNotes) |
| [List Patient Free-Text Notes by Type](actions/list-patient-free-text-notes-by-type.md) | `GET /patients/:patient_id/pt_notes/:pt_note_type_id` | [docs](https://docs.cer.bo/#tag/Patient-Free-Text-Notes/operation/showPatientNote) |
| [List Patient Health Maintenance Readings](actions/list-patient-health-maintenance-readings.md) | `GET /patients/:patient_id/health_maintenance` | [docs](https://docs.cer.bo/#tag/Patient-Health-Maintenance/operation/showPatientHealthMaintenance) |
| [List Patient Height Vitals](actions/list-patient-height-vitals.md) | `GET /patients/:patient_id/vitals/height` | [docs](https://docs.cer.bo/#tag/Patient-Vitals/operation/listPatientHeightVitals) |
| [List Patient Images](actions/list-patient-images.md) | `GET /patients/:patient_id/images` | [docs](https://docs.cer.bo/#tag/Patient-Images/operation/listPatientImages) |
| [List Patient Invoices](actions/list-patient-invoices.md) | `GET /patients/:patient_id/invoices` | [docs](https://docs.cer.bo/#tag/Patient-Invoices/operation/listPatientInvoices) |
| [List Patient Lab Results](actions/list-patient-lab-results.md) | `GET /patients/:pt_id/lab_results` | [docs](https://docs.cer.bo/#tag/Patient-Lab-Results/operation/getPatientLabResults) |
| [List Patient Laboratories](actions/list-patient-laboratories.md) | `GET /patients/:patient_id/laboratories` | [docs](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/listPatientFacilities) |
| [List Patient Note Types](actions/list-patient-note-types.md) | `GET /pt_notes` | [docs](https://docs.cer.bo/#tag/Patient-Free-Text-Notes/operation/listPatientNotes) |
| [List Patient Orders](actions/list-patient-orders.md) | `GET /patients/:patient_id/orders` | [docs](https://docs.cer.bo/#tag/Patient-Orders/operation/listPatientOrders) |
| [List Patient Past Medical History](actions/list-patient-past-medical-history.md) | `GET /patients/:patient_id/pmh` | [docs](https://docs.cer.bo/#tag/Patient-Past-Medical-History/operation/listPatientPastMedicalHistory) |
| [List Patient Pharmacies](actions/list-patient-pharmacies.md) | `GET /patients/:patient_id/pharmacies` | [docs](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/listPatientPharmacies) |
| [List Patient Prescriptions](actions/list-patient-prescriptions.md) | `GET /patients/:patient_id/rxs` | [docs](https://docs.cer.bo/#tag/Patient-Prescriptions/operation/listPatientPrescriptions) |
| [List Patient Questionnaires](actions/list-patient-questionnaires.md) | `GET /patients/:patient_id/questionnaires` | [docs](https://docs.cer.bo/#tag/Questionnaires/operation/listPatientQuestionnaires) |
| [List Patient Specialists](actions/list-patient-specialists.md) | `GET /patients/:patient_id/specialists` | [docs](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/listPatientSpecialists) |
| [List Patient Subscriptions](actions/list-patient-subscriptions.md) | `GET /patients/:patient_id/subscriptions` | [docs](https://docs.cer.bo/#tag/Patient-Subscriptions/operation/showPatientSubscriptions) |
| [List Patient Supplements](actions/list-patient-supplements.md) | `GET /patients/:patient_id/supplements` | [docs](https://docs.cer.bo/#tag/Patient-Supplements/operation/listPatientSupplements) |
| [List Patient Tags](actions/list-patient-tags.md) | `GET /patients/:patient_id/tags` | [docs](https://docs.cer.bo/#tag/Patient-Tags/operation/listPatientTags) |
| [List Patient Vaccines](actions/list-patient-vaccines.md) | `GET /patients/:patient_id/vaccines` | [docs](https://docs.cer.bo/#tag/Patient-Vaccines/operation/listPatientVaccines) |
| [List Patient Weight Vitals](actions/list-patient-weight-vitals.md) | `GET /patients/:patient_id/vitals/weight` | [docs](https://docs.cer.bo/#tag/Patient-Vitals/operation/listPatientWeightVitals) |
| [List Patients](actions/list-patients.md) | `GET /patients` | [docs](https://docs.cer.bo/#tag/Patients/operation/listPatients) |
| [List Portal Requests](actions/list-portal-requests.md) | `GET /patients/:pt_id/portal/enqueued` | [docs](https://docs.cer.bo/#tag/Patient-Portal/operation/showPortalRequests) |
| [List Secure Messages](actions/list-secure-messages.md) | `GET /patients/:patient_id/portal/secure_messages` | [docs](https://docs.cer.bo/#tag/Secure-Messages/operation/listSecureMessages) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /patients/subscriptions` | [docs](https://docs.cer.bo/#tag/Patient-Subscriptions/operation/listPatientSubscriptions) |
| [List Supplements](actions/list-supplements.md) | `GET /supplements` | [docs](https://docs.cer.bo/#tag/Supplements/operation/listSupplements) |
| [List System-Wide Charges](actions/list-system-wide-charges.md) | `GET /charges` | [docs](https://docs.cer.bo/#tag/Charges/operation/listAllCharges) |
| [List Tag Definitions](actions/list-tag-definitions.md) | `GET /tags` | [docs](https://docs.cer.bo/#tag/Tags/operation/listTags) |
| [List Tasks](actions/list-tasks.md) | `GET /task` | [docs](https://docs.cer.bo/#tag/Tasks/operation/listTasks) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.cer.bo/#tag/Users/operation/listUsers) |
| [List Vitals Tag Groups](actions/list-vitals-tag-groups.md) | `GET /vitals_tag_groups` | [docs](https://docs.cer.bo/#tag/Vitals/operation/listVitalsTagGroups) |
| [Queue Patient Prescription](actions/queue-patient-prescription.md) | `POST /patients/:patient_id/rxs` | [docs](https://docs.cer.bo/#tag/Patient-Prescriptions/operation/queuePatientPrescription) |
| [Queue Patient Supplement](actions/queue-patient-supplement.md) | `POST /patients/:patient_id/supplements` | [docs](https://docs.cer.bo/#tag/Patient-Supplements/operation/queuePatientSupplement) |
| [Refill Patient Prescription](actions/refill-patient-prescription.md) | `POST /patients/:patient_id/rxs/refill` | [docs](https://docs.cer.bo/#tag/Patient-Prescriptions/operation/refillPatientPrescription) |
| [Search Drugs](actions/search-drugs.md) | `GET /drugs/search/:term` | [docs](https://docs.cer.bo/#tag/Drugs/operation/searchDrugs) |
| [Search Patients](actions/search-patients.md) | `GET /patients/search` | [docs](https://docs.cer.bo/#tag/Patients/operation/searchPatients) |
| [Search Supplements](actions/search-supplements.md) | `GET /supplements/search/:terms` | [docs](https://docs.cer.bo/#tag/Supplements/operation/searchSupplements) |
| [Send Patient Email](actions/send-patient-email.md) | `POST /patients/:patient_id/emails/send` | [docs](https://docs.cer.bo/#tag/Patient-Emails/operation/sendPatientEmail) |
| [Stream Patient Document](actions/stream-patient-document.md) | `GET /documents/:document_id/stream` | [docs](https://docs.cer.bo/#tag/Patient-Documents/operation/streamPatientDocument) |
| [Stream Patient Image](actions/stream-patient-image.md) | `GET /patients/:patient_id/images/:image_id/stream` | [docs](https://docs.cer.bo/#tag/Patient-Images/operation/streamPatientImage) |
| [Update Appointment](actions/update-appointment.md) | `PATCH /appointments/:appointment_id` | [docs](https://docs.cer.bo/#tag/Appointments/operation/updateAppointment) |
| [Update Inventory](actions/update-inventory.md) | `PATCH /inventory/:id` | [docs](https://docs.cer.bo/#tag/Inventory/operation/updateInventory) |
| [Update Patient](actions/update-patient.md) | `PATCH /patients/:patient_id` | [docs](https://docs.cer.bo/#tag/Patients/operation/updatePatient) |
| [Update Patient Note](actions/update-patient-note.md) | `POST /patients/:patient_id/pt_notes/:pt_note_type_id` | [docs](https://docs.cer.bo/#tag/Patient-Free-Text-Notes/operation/updatePatientNote) |
| [Update Patient Tags](actions/update-patient-tags.md) | `POST /patients/:patient_id/tags` | [docs](https://docs.cer.bo/#tag/Patient-Tags/operation/updatePatientTags) |
| [Update Supplement](actions/update-supplement.md) | `PATCH /supplements/:supplement_id` | [docs](https://docs.cer.bo/#tag/Supplements/operation/updateSupplement) |
| [Update Tag](actions/update-tag.md) | `PATCH /tags/:tag_id` | [docs](https://docs.cer.bo/#tag/Tags/operation/updateTag) |
| [Update Task](actions/update-task.md) | `PATCH /task/:task_id` | [docs](https://docs.cer.bo/#tag/Tasks/operation/updateTask) |
| [Validate Portal Credentials](actions/validate-portal-credentials.md) | `POST /patients/portal/validate_credentials` | [docs](https://docs.cer.bo/#tag/Patient-Portal/operation/validatePortalCredentials) |
| [Validate User Credentials](actions/validate-user-credentials.md) | `POST /users/validate_credentials` | [docs](https://docs.cer.bo/#tag/Users/operation/validateUserCredentials) |
