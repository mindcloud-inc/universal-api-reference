# Update Tag with Systeme.io

Updates an existing tag in Systeme.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/tags/:id`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [Update Tag](https://developer.systeme.io/reference/api_tags_id_put-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Tag identifier. |
| `name` | body | `string` | yes | New tag name. |
