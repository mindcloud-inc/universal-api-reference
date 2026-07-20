# Upsert Participant Study Data Collection with Castor EDC

Updates participant study data in Castor EDC.

## Endpoint

- **Method:** `POST`
- **Path:** `/study/:study_id/participant/:participant_id/data-points/study`
- **Base URL:** `https://us.castoredc.com/api`
- **Official documentation:** [Upsert Participant Study Data Collection](https://us.castoredc.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `study_id` | path | `string` | yes | The Castor study UUID. |
| `participant_id` | path | `string` | yes | The participant UUID. |
| `common` | body | `object` | no | Optional common parameters object for change_reason and confirmed_changes. |
| `data[]` | body | `array<object>` | yes | Array of study data point objects with field_id and field_value. |
