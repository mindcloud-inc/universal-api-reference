# Get Latest Pixel with Pixela

Retrieves the latest pixel from a Pixela graph.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/:username/graphs/:graphID/latest`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Get Latest Pixel](https://docs.pixe.la/entry/get-latest-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
