# Update Custom Color with Instructure

Updates a custom color in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/self/colors/:asset_string`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Custom Color](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.set_custom_color)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_string` | path | `string` | yes | Asset string for the custom color entry. |
| `hexcode` | body | `string` | yes | Hex color code to assign. |
