# Move Section with Filestage

Moves a section to a new position in Filestage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/{projectId}/sections/{sectionId}/position`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Move Section](https://developers.filestage.io/docs/api/p3sv3uy7khxb5-move-section)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sectionId` | path | `string` | yes | — |
| `projectId` | path | `string` | yes | — |
| `position` | body | `number` | yes | This is the preferred position. Given that `0 <= position < E`, where E is the number of sections in the project. |
