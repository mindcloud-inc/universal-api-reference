# List Graphs with Pixela

Retrieves all graph definitions in Pixela.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/:username/graphs`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [List Graphs](https://docs.pixe.la/entry/get-graph)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. Use the Pixela username, not an email address. Maximum length: 33. |
