# Increment Pixel with Pixela

Increments today's pixel in Pixela using the graph timezone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/users/:username/graphs/:graphID/increment`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Increment Pixel](https://docs.pixe.la/entry/increment-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
