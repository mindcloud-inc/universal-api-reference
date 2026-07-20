# Update Tag with Rebrandly

Updates an existing tag in Rebrandly.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/:id`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Update Tag](https://developers.rebrandly.com/docs/updating-a-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the tag to update. |
| `name` | body | `string` | yes | New unique name of the tag. |
| `color` | body | `string` | yes | 6-digit hexadecimal color assigned to the tag. |
