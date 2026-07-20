# Get Pixel with Pixela

Retrieves a pixel from a Pixela graph by date.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/:username/graphs/:graphID/:yyyyMMdd`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Get Pixel](https://docs.pixe.la/entry/get-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
| `yyyyMMdd` | path | `string` | yes | Pixel date in yyyyMMdd format. |
