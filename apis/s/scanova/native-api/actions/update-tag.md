# Update Tag with Scanova

## Endpoint

- **Method:** `PUT`
- **Path:** `/tags/{tag_id}/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Update Tag](https://docs.scanova.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag_id` | path | `number` | yes | Tag ID |
| `name` | body | `string` | no | Tag name |
| `color` | body | `string` | no | Tag color (hex code) |
