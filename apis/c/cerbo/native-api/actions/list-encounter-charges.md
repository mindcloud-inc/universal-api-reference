# List Encounter Charges with Cerbo

Retrieves encounter charges from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:pt_id/encounters/:encounter_id/charges`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Encounter Charges](https://docs.cer.bo/#tag/Charges/operation/listEncounterCharges)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pt_id` | path | `number` | yes | The ID of the patient. |
| `encounter_id` | path | `number` | yes | The ID of the encounter. |
