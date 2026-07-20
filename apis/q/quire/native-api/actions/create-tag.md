# Create Tag with Quire

Creates a new tag in Quire.

## Endpoint

- **Method:** `POST`
- **Path:** `tag/id/:projectId`
- **Base URL:** `https://quire.io/api`
- **Official documentation:** [Create Tag](https://quire.io/dev/api/#operation--tag-id--projectId--post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The project ID or shortcut, for example App_Account. |
| `name` | body | `string` | yes | The display name for the new tag. |
| `global` | body | `boolean` | no | Whether the tag should be available across projects. |
| `color` | body | `string` | no | Optional Quire color code such as 35. |
