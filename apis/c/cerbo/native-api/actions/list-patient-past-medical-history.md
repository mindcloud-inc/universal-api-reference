# List Patient Past Medical History with Cerbo

Retrieves patient past medical history from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/pmh`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Past Medical History](https://docs.cer.bo/#tag/Patient-Past-Medical-History/operation/listPatientPastMedicalHistory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
