# List Patient Blood Pressure Vitals with Cerbo

Retrieves patient blood pressure vitals from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/vitals/bp`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Blood Pressure Vitals](https://docs.cer.bo/#tag/Patient-Vitals/operation/listPatientBloodPressureVitals)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `patient_id` | path | `number` | no |
