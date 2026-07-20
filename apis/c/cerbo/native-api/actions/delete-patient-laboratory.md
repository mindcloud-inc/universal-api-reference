# Delete Patient Laboratory with Cerbo

Deletes a patient laboratory from Cerbo.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/patients/:patient_id/laboratories/:patient_laboratory_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Delete Patient Laboratory](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/deletePatientFacility)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | ID of the patient |
| `patient_laboratory_id` | path | `number` | yes | ID of the patient laboratory association |
