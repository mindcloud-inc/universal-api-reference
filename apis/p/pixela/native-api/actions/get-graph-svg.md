# Get Graph SVG with Pixela

Retrieves a Pixela graph as an SVG diagram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/:username/graphs/:graphID`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Get Graph SVG](https://docs.pixe.la/entry/get-svg)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
