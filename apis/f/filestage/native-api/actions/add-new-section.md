# Add New Section with Filestage

Creates a new section in a Filestage project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{projectId}/sections`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Add New Section](https://developers.filestage.io/docs/api/vcqwuhq2ejw8y-add-new-section)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project Id |
| `sectionName` | body | `string` | yes | — |
