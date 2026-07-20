# Get Graph Definition with Pixela

Retrieves a graph definition from Pixela.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/:username/graphs/:graphID/graph-def`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Get Graph Definition](https://docs.pixe.la/entry/get-graph-def)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
