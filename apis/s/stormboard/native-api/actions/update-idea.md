# Update Idea with Stormboard

Updates an idea in Stormboard.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ideas/:idea_id`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Update Idea](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | Updated idea color. |
| `data` | body | `string` | no | Updated idea content or media data. |
| `idea_id` | path | `number` | yes | Idea ID from a Stormboard idea record. |
| `lock` | body | `number` | no | Set to 1 to lock the idea, or 0 to leave it unlocked. |
| `shape` | body | `string` | no | Updated idea shape. |
| `type` | body | `string` | no | Updated idea type. |
| `x` | body | `number` | no | Updated X position. |
| `y` | body | `number` | no | Updated Y position. |
