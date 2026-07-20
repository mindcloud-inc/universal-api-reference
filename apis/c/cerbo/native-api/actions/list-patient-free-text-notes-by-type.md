# List Patient Free-Text Notes by Type with Cerbo

Retrieves patient free-text notes by type from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/pt_notes/:pt_note_type_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Free-Text Notes by Type](https://docs.cer.bo/#tag/Patient-Free-Text-Notes/operation/showPatientNote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `pt_note_type_id` | path | `number` | no | ID of note type |
