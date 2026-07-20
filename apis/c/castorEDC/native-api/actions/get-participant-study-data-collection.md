# Get Participant Study Data Collection with Castor EDC

Retrieves study data for a participant in Castor EDC.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/participant/:participant_id/data-points/study`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Get Participant Study Data Collection](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `participant_id` | path | `string` | yes | The participant UUID. |
| `field_ids` | query | `string` | no | Comma-separated list of field UUIDs to include. Send multiple values as a string separated by `,`. |
| `updated_after` | query | `string` | no | Only return data points updated strictly after this ISO 8601 timestamp. |
