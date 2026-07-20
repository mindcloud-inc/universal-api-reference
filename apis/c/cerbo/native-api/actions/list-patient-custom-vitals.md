# List Patient Custom Vitals with Cerbo

Retrieves patient custom vitals from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/vitals/:vital_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Custom Vitals](https://docs.cer.bo/#tag/Patient-Vitals/operation/listPatientCustomVitals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | ID of patient |
| `vital_id` | path | `number` | yes | — |
