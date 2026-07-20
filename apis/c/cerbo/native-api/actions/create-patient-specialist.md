# Create Patient Specialist with Cerbo

Creates a patient specialist record in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/specialists`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Patient Specialist](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/createPatientSpecialist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | The patient ID |
| `specialist_id` | body | `number` | yes | The specialist ID from the master specialists database. Use the facilities/specialists endpoints to find valid IDs. |
| `priority_order` | body | `number` | no | Position in the patient's specialist list (lower = higher priority). If provided, `set_as_primary` is ignored. |
| `set_as_primary` | body | `boolean` | no | If true, adds to top of list (priority). If false, adds to bottom. Only used when `priority_order` is not provided. |
| `note` | body | `string` | no | Optional note about this specialist for the patient (max 255 characters) |
