# List Comments with Stormboard

Retrieves comments for an idea in Stormboard.

## Endpoint

- **Method:** `GET`
- **Path:** `/ideas/:idea_id/comments`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [List Comments](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `avatars` | query | `number` | no | Set to 1 to include user avatar data, or 0 to skip it. |
| `idea_id` | path | `number` | yes | Idea ID from a Stormboard idea record. |
| `order` | query | `string` | no | Sort comment order: asc or desc. |
