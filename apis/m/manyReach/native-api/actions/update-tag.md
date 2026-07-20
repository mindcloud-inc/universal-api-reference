# Update Tag with ManyReach

Updates an existing tag in ManyReach.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.manyreach.com/api/v2/tags/:id`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Update Tag](https://api.manyreach.com/api#v2/tag/tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Tag ID. |
| `title` | body | `string` | no | Updated tag title. |
