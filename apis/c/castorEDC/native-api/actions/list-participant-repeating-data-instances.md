# List Participant Repeating Data Instances with Castor EDC

Retrieves repeating data instances for a participant in Castor EDC.

## Endpoint

- **Method:** `GET`
- **Path:** `/study/:study_id/participant/:participant_id/repeating-data-instance`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [List Participant Repeating Data Instances](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `participant_id` | path | `string` | yes | The participant UUID. |
| `page` | query | `number` | no | Page number to retrieve. |
| `archived` | query | `number` | no | 0 for unarchived instances, 1 for archived instances. |
