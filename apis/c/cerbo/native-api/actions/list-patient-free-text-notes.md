# List Patient Free-Text Notes with Cerbo

Retrieves patient free-text notes from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/pt_notes`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Free-Text Notes](https://docs.cer.bo/#tag/Patient-Free-Text-Notes/operation/listAllPatientNotes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
