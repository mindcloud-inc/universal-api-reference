# Create Graph with Pixela

Creates a new graph definition in Pixela.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/:username/graphs`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Create Graph](https://docs.pixe.la/entry/post-graph)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `id` | body | `string` | yes | Graph ID. Must match ^[a-z][a-z0-9-]{1,16}. |
| `name` | body | `string` | yes | Graph display name. |
| `unit` | body | `string` | yes | Unit for recorded quantities, such as commit or kilogram. |
| `type` | body | `string` | yes | Quantity type. Pixela supports int or float. |
| `color` | body | `string` | yes | Graph color: shibafu, momiji, sora, ichou, ajisai, or kuro. |
