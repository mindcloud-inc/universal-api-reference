# Create Participant with Castor EDC

Creates a participant in Castor EDC.

## Endpoint

- **Method:** `POST`
- **Path:** `/study/:study_id/participant`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Create Participant](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ccr_patient_id` | body | `string` | no | Optional clinical identifier |
| `participant_id` | body | `string` | no | Participant identifier when the study allows free-text IDs |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `site_id` | body | `string` | yes | Site UUID for the participant |
| `email_address` | body | `string` | no | Optional participant email address |
