# Add To Pixel with Pixela

Adds quantity to today's Pixela pixel using the graph timezone.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/users/:username/graphs/:graphID/add`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Add To Pixel](https://docs.pixe.la/entry/add-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
| `quantity` | body | `string` | yes | Quantity to add to today's pixel. |
