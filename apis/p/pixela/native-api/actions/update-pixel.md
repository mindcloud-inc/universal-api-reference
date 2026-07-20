# Update Pixel with Pixela

Updates a pixel in Pixela, or creates it if missing.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/users/:username/graphs/:graphID/:yyyyMMdd`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Update Pixel](https://docs.pixe.la/entry/put-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quantity` | body | `string` | no | Quantity to set for the pixel. |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
| `yyyyMMdd` | path | `string` | yes | Pixel date in yyyyMMdd format. |
