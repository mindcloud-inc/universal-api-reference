# Create Template with GatherContent

Creates a new template in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/templates`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Create Template](https://docs.gathercontent.com/reference/createtemplate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Template name. |
| `project_id` | path | `string` | yes | Project id. |
| `structure` | body | `string` | no | Template structure object. |
