# Alter Structure with GatherContent

Updates a structure in GatherContent and applies changes to items.

## Endpoint

- **Method:** `PUT`
- **Path:** `/structures/:structure_uuid`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Alter Structure](https://docs.gathercontent.com/reference/alterstructure)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `structure` | body | `string` | yes | Structure object. |
| `structure_uuid` | path | `string` | yes | Structure UUID. |
