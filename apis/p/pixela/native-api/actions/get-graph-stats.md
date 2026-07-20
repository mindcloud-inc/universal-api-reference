# Get Graph Stats with Pixela

Retrieves statistics for a Pixela graph.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/:username/graphs/:graphID/stats`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Get Graph Stats](https://docs.pixe.la/entry/get-graph-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
