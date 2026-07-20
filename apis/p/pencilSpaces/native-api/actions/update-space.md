# Update Space with Pencil Spaces

## Endpoint

- **Method:** `PATCH`
- **Path:** `/spaces/:spaceId`
- **Base URL:** `https://apis.pencilapp.com/public/api`
- **Official documentation:** [Update Space](https://api.pencilspaces.com/guide/spaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | body | `object` | no | Container for mutable Space fields. |
| `space.archived` | body | `boolean` | no | Whether the Space should be archived. |
| `space.title` | body | `string` | no | Updated title for the Space. |
| `space.visibility` | body | `string` | no | Updated visibility for the Space. |
| `spaceId` | path | `string` | yes | The Pencil spaceId of the Space to update. |
