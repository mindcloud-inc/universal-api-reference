# Update Screenshot with Diffy

Updates a screenshot name in Diffy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/snapshots/:id`
- **Base URL:** `https://app.diffy.website/api`
- **Official documentation:** [Update Screenshot](https://app.diffy.website/rest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Screenshot ID. |
| `name` | body | `string` | no | Updated screenshot name. |
