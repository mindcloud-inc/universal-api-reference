# Subtract From Pixel with Pixela

Subtracts quantity from today's Pixela pixel using the graph timezone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/users/:username/graphs/:graphID/subtract`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Subtract From Pixel](https://docs.pixe.la/entry/subtract-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
| `quantity` | body | `string` | yes | Quantity to subtract from today's pixel. |
