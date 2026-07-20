# List Graph Pixels with Pixela

Retrieves pixels from a Pixela graph by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/:username/graphs/:graphID/pixels`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [List Graph Pixels](https://docs.pixe.la/entry/get-graph-pixels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | path | `string` | yes | Pixela graph identifier. |
| `from` | query | `string` | no | Start date in yyyyMMdd format. |
| `to` | query | `string` | no | End date in yyyyMMdd format. |
