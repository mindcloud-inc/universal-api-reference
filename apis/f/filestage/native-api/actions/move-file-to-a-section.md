# Move File to a Section with Filestage

Moves a Filestage file to a section.

## Endpoint

- **Method:** `PUT`
- **Path:** `/files/{fileId}/section`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Move File to a Section](https://developers.filestage.io/docs/api/mi9lh0smo12di-move-file-to-a-section)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | File Id |
| `sectionId` | body | `string` | no | The ID of the section to move the file into. |
