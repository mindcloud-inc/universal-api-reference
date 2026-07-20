# Exit Lead from Pipeline Successfully with Nimble

Marks a lead as successfully exited from a Nimble pipeline.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/leads/:lead_id/:pipeline_id/successful`
- **Base URL:** `https://app.nimble.com`
- **Official documentation:** [Exit Lead from Pipeline Successfully](https://www.nimble.com/developers/docs/#tag/Contacts-Pipelines/operation/mark-lead-exited-successful)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `string` | yes | Nimble lead_id path parameter. |
| `pipeline_id` | path | `string` | yes | Nimble pipeline_id path parameter. |
| `actual_exit_date` | body | `date` | no | — |
| `notes` | body | `string` | no | — |
