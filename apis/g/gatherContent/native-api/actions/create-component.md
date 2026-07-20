# Create Component with GatherContent

Creates a new component in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/components`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Create Component](https://docs.gathercontent.com/reference/createcomponent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields[]` | body | `array<object>` | yes | Component fields definition. |
| `name` | body | `string` | yes | Component name. |
| `project_id` | path | `string` | yes | Project id. |
