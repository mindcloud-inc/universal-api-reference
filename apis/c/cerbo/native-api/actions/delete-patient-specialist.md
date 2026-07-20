# Delete Patient Specialist with Cerbo

Deletes a patient specialist from Cerbo.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/patients/:patient_id/specialists/:patient_specialist_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Delete Patient Specialist](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/deletePatientSpecialist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | The patient ID |
| `patient_specialist_id` | path | `number` | yes | The patient-specialist association ID (not the specialist ID) |
