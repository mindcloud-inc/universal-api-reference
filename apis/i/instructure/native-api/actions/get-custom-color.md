# Get Custom Color with Instructure

Retrieves a custom color from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/self/colors/:asset_string`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get Custom Color](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.get_custom_color)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_string` | path | `string` | yes | Asset string for the custom color entry. |
