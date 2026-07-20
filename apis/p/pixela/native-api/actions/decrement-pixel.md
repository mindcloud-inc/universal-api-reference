# Decrement Pixel with Pixela

Decrements today's pixel in Pixela using the graph timezone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/users/:username/graphs/:graphID/decrement`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Decrement Pixel](https://docs.pixe.la/entry/decrement-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
