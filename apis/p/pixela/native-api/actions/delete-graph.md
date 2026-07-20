# Delete Graph with Pixela

Deletes an existing graph definition from Pixela.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/users/:username/graphs/:graphID`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Delete Graph](https://docs.pixe.la/entry/delete-graph)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
