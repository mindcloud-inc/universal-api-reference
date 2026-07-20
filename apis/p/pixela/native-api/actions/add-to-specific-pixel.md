# Add To Specific Pixel with Pixela

Adds quantity to a specific Pixela pixel by date.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/users/:username/graphs/:graphID/:yyyyMMdd/add`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Add To Specific Pixel](https://docs.pixe.la/entry/add-specific-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
| `yyyyMMdd` | path | `string` | yes | Pixel date in yyyyMMdd format. |
| `quantity` | body | `string` | yes | Quantity to add to the pixel. |
