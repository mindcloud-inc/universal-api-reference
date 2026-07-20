# List Encounter Types with Cerbo

Retrieves encounter types from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/encounter_types`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Encounter Types](https://docs.cer.bo/#tag/Encounter-Types/operation/listEncounterTypes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_deleted` | query | `boolean` | no | When set to any truthy value, includes soft-deleted encounter types in the response. |
