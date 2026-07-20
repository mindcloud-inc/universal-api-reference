# List Encounter Estimates with Cerbo

Retrieves encounter estimates from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:pt_id/encounters/:encounter_id/estimates`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Encounter Estimates](https://docs.cer.bo/#tag/Patient-Charges/operation/listEncounterEstimates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pt_id` | path | `number` | no |
| `encounter_id` | path | `number` | no |
