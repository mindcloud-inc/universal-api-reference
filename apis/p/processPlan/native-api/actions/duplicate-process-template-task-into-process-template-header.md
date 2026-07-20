# Duplicate Process Template Task into Process Template Header with Process Plan

## Endpoint

- **Method:** `POST`
- **Path:** `/process_template_task/:processTemplateTaskId/duplicate/into/process_template_header/:processTemplateHeaderId`
- **Base URL:** `https://apius0.processplan.com/api/v4`
- **Official documentation:** [Duplicate Process Template Task into Process Template Header](https://answers.processplan.com/c/api/api-endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processTemplateHeaderId` | path | `string` | no | Process template header ID. |
| `processTemplateTaskId` | path | `string` | no | Process template task ID. |
