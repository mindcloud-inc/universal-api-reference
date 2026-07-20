# Rename Section with Filestage

Updates a section name in Filestage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/{projectId}/sections/{sectionId}`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Rename Section](https://developers.filestage.io/docs/api/3suhqt87go17q-rename-section)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project Id |
| `sectionId` | path | `string` | yes | Section Id |
| `name` | body | `string` | no | The new name for the section |
