# Create Pixel with Pixela

Creates a new pixel in a Pixela graph.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/:username/graphs/:graphID`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Create Pixel](https://docs.pixe.la/entry/post-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
| `date` | body | `string` | yes | Pixel date in yyyyMMdd format. |
| `quantity` | body | `string` | yes | Quantity to record for the pixel. |
