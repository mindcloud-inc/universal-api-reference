# List Patient Specialists with Cerbo

Retrieves patient specialists from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/specialists`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Specialists](https://docs.cer.bo/#tag/Patient-FacilitiesSpecialists/operation/listPatientSpecialists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | The patient ID |
