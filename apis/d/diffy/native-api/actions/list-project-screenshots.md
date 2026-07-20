# List Project Screenshots with Diffy

Retrieves screenshots for a project from Diffy.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:id/screenshots`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [List Project Screenshots](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Project ID. |
| `page` | query | `number` | no | Page number, starting at 0. |
