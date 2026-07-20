# Move Lead To Pipeline Stage with Nimble

Moves a lead to a pipeline stage in Nimble.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/leads/:lead_id/:pipeline_id/move`
- **Base URL:** `https://app.nimble.com`
- **Official documentation:** [Move Lead To Pipeline Stage](https://www.nimble.com/developers/docs/#tag/Contacts-Pipelines/operation/move-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `string` | yes | Nimble lead_id path parameter. |
| `pipeline_id` | path | `string` | yes | Nimble pipeline_id path parameter. |
| `stage_id` | body | `string` | yes | — |
