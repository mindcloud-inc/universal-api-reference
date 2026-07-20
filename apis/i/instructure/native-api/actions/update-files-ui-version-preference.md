# Update Files UI Version Preference with Instructure

Updates the Files UI version preference in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/self/files_ui_version_preference`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Files UI Version Preference](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.set_files_ui_version_preference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files_ui_version` | body | `string` | yes | Preferred files UI version. |
