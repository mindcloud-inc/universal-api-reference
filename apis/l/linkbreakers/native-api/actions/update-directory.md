# Update a Directory with Linkbreakers

Updates an existing directory in Linkbreakers.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/directories/:id`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Update a Directory](https://linkbreakers.com/help/api/directories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the directory to update. |
| `name` | body | `string` | no | The new name of the directory. |
| `parentDirectoryId` | body | `string` | no | The parent directory ID. |
| `parentDirectoryIdDelete` | body | `boolean` | no | Remove the parent directory association. |
