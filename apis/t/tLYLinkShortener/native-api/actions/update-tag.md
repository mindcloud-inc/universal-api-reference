# Update Tag with TLY Link Shortener

Updates an existing tag in TLY Link Shortener.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/link/tag/:id`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Update Tag](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The tag ID to update. |
| `tag` | body | `string` | yes | The updated tag name. |
