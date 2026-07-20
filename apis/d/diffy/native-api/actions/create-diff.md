# Create Diff with Diffy

Creates a screenshot diff in Diffy.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:id/diffs`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [Create Diff](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Project ID. |
| `name` | body | `string` | no | Custom diff name. |
| `snapshot1` | body | `number` | yes | First screenshot ID. |
| `snapshot2` | body | `number` | yes | Second screenshot ID. |
