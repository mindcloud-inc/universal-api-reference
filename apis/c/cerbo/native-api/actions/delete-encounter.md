# Delete Encounter with Cerbo

Deletes an existing encounter from Cerbo.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/encounters/:encounter_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Delete Encounter](https://docs.cer.bo/#tag/Encounters/operation/deleteEncounter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `encounter_id` | path | `number` | yes | Encounter identifier. |
