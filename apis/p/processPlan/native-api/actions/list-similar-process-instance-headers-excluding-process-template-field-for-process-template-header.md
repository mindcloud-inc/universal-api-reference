# List Similar Process Instance Headers Excluding Process Template Field for Process Template Header with Process Plan

## Endpoint

- **Method:** `GET`
- **Path:** `/process_template_header/:processTemplateHeaderId/similar_to/process_instance_header/:processInstanceHeaderId/excluding/process_template_field/:processTemplateFieldId`
- **Base URL:** `https://apius0.processplan.com/api/v4`
- **Official documentation:** [List Similar Process Instance Headers Excluding Process Template Field for Process Template Header](https://answers.processplan.com/c/api/api-endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processInstanceHeaderId` | path | `string` | no | Process instance header ID. |
| `processTemplateFieldId` | path | `string` | no | Process template field ID. |
| `processTemplateHeaderId` | path | `string` | no | Process template header ID. |
