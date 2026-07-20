# List Project Diffs with Diffy

Retrieves diffs for a project from Diffy.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:id/diffs`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [List Project Diffs](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Project ID. |
| `page` | query | `number` | no | Page number, starting at 0. |
