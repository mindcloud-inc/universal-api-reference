# Bulk Assign Links To Collection with LinkTwin

Adds or removes multiple links for a collection in LinkTwin.

## Endpoint

- **Method:** `POST`
- **Path:** `/collection/:id/links`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Bulk Assign Links To Collection](https://linktw.in/developers#bulk-assign-links-to-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Collection ID. |
| `add[]` | body | `array<number>` | no | Link IDs to add. |
| `remove[]` | body | `array<number>` | no | Link IDs to remove. |
