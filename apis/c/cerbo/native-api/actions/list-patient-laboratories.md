# List Patient Laboratories with Cerbo

Retrieves patient laboratories from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/laboratories`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Laboratories](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/listPatientFacilities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | ID of the patient |
