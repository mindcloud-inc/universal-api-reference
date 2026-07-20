# Create Record with Castor EDC

Creates a record in Castor EDC.

## Endpoint

- **Method:** `POST`
- **Path:** `/study/:study_id/record`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Create Record](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ccr_patient_id` | body | `string` | no | Optional clinical identifier |
| `record_id` | body | `string` | no | Record identifier when the study allows free-text IDs |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `institute_id` | body | `string` | yes | Institute UUID for the record |
| `email_address` | body | `string` | no | Optional record email address |
