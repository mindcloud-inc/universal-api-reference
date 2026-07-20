# Create Multiple Pixels with Pixela

Creates multiple pixels in a Pixela graph.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/:username/graphs/:graphID/pixels`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Create Multiple Pixels](https://docs.pixe.la/entry/batch-post-pixels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
| `pixels[]` | body | `array<object>` | yes | Array of pixel objects. Maximum 365 pixels per request. |
