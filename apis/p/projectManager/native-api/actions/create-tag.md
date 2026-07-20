# Create Tag with ProjectManager

Creates a new tag in ProjectManager.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/data/tags`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Create Tag](https://developer.projectmanager.com/api-reference/tag/create-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of this Tag. |
| `color` | body | `string` | no | The color that will be used to represent this Tag visually.  This color is automatically chosen by the application when a user creates a Tag.              You can choose specify any color that can be represented using HTML RGB syntax such as `#0088FF`, in the format `RRGGBB`.  You may not use names for colors. |
