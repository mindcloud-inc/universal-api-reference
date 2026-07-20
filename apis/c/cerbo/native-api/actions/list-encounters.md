# List Encounters with Cerbo

Retrieves patient encounters from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/encounters`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Encounters](https://docs.cer.bo/#tag/Encounters/operation/listEncounters)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | yes | The ID of the patient. |
| `type` | query | `string` | no | Limit results to a specific encounter note type (e.g., "ov" for office visit). |
| `signed_only` | query | `boolean` | no | If included and set to "false," return all encounter notes, including those not marked as signed. |
