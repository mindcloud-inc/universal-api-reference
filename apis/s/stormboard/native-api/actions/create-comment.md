# Create Comment with Stormboard

Creates a comment on an idea in Stormboard.

## Endpoint

- **Method:** `POST`
- **Path:** `/ideas/:idea_id/comments`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Create Comment](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment` | body | `string` | yes | Comment text to post on the idea. |
| `idea_id` | path | `number` | yes | Idea ID from a Stormboard idea record. |
