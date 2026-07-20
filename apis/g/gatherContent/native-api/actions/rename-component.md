# Rename Component with GatherContent

Renames an existing component in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/components/:component_uuid/rename`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Rename Component](https://docs.gathercontent.com/reference/renamecomponent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component_uuid` | path | `string` | yes | Component UUID. |
| `name` | body | `string` | yes | Component name. |
