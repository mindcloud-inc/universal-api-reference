# Update Tag with ProjectManager

Updates an existing tag in ProjectManager.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/data/tags/:tagId`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Update Tag](https://developer.projectmanager.com/api-reference/tag/update-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagId` | path | `string` | yes | The id of the tag |
| `color` | body | `string` | no | The color that will be used to represent this Tag visually.  This color is automatically chosen by the application when a user creates a Tag.              You can choose specify any color that can be represented using HTML RGB syntax such as `#0088FF`, in the format `RRGGBB`.  You may not use names for colors. |
