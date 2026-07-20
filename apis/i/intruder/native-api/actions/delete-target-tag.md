# Delete Target Tag with Intruder

## Endpoint

- **Method:** `DELETE`
- **Path:** `/targets/:target_id/tags/:name/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Delete Target Tag](https://developers.intruder.io/reference/targets_tags_destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_id` | path | `string` | yes | The Intruder target identifier. |
| `name` | path | `string` | yes | The tag name to delete from the target. |
