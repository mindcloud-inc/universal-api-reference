# Subtract From Specific Pixel with Pixela

Subtracts quantity from a specific Pixela pixel by date.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/users/:username/graphs/:graphID/:yyyyMMdd/subtract`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Subtract From Specific Pixel](https://docs.pixe.la/entry/subtract-specific-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
| `yyyyMMdd` | path | `string` | yes | Pixel date in yyyyMMdd format. |
| `quantity` | body | `string` | yes | Quantity to subtract from the pixel. |
