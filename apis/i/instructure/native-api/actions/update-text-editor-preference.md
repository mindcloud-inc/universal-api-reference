# Update Text Editor Preference with Instructure

Updates the text editor preference in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/self/text_editor_preference`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Text Editor Preference](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.set_text_editor_preference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text_editor_preference` | body | `string` | yes | Preferred text editor mode. |
