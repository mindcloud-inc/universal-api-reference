# Delete Pixel with Pixela

Deletes an existing pixel from a Pixela graph.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/users/:username/graphs/:graphID/:yyyyMMdd`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Delete Pixel](https://docs.pixe.la/entry/delete-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
| `yyyyMMdd` | path | `string` | yes | Pixel date in yyyyMMdd format. |
