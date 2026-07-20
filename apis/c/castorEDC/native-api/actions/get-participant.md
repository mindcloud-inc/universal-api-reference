# Get Participant with Castor EDC

Retrieves a participant from Castor EDC by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/participant/:participant_id`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Get Participant](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The ID of the study for which this call should be made |
| `participant_id` | path | `string` | yes | Participant ID of the Participant to fetch |
