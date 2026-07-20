# Update Patient Note with Cerbo

Updates a patient free-text note in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/patients/:patient_id/pt_notes/:pt_note_type_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Update Patient Note](https://docs.cer.bo/#tag/Patient-Free-Text-Notes/operation/updatePatientNote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
| `pt_note_type_id` | path | `number` | no | ID of note type |
| `note` | body | `string` | yes | The new free-text note value |
