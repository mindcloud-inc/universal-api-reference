# Update Component Fields with GatherContent

Updates fields for an existing component in GatherContent.

## Endpoint

- **Method:** `PUT`
- **Path:** `/components/:component_uuid/fields`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Update Component Fields](https://docs.gathercontent.com/reference/updatecomponentfields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component_uuid` | path | `string` | yes | Component UUID. |
| `fields[]` | body | `array<object>` | yes | Component fields definition. |
