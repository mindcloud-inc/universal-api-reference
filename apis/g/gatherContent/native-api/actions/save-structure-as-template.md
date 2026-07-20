# Save Structure As Template with GatherContent

Creates a template from a structure in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/structures/:structure_uuid/templates`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Save Structure As Template](https://docs.gathercontent.com/reference/savestructureastemplate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Template name. |
| `structure_uuid` | path | `string` | yes | Structure UUID. |
