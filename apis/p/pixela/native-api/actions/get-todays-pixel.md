# Get Today's Pixel with Pixela

Retrieves today's pixel from a Pixela graph.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/:username/graphs/:graphID/today`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Get Today's Pixel](https://docs.pixe.la/entry/get-today-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
