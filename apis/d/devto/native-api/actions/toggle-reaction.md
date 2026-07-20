# Toggle Reaction with Dev.to

Toggles the authenticated user's reaction to an article, comment, or user in Dev.to.

## Endpoint

- **Method:** `POST`
- **Path:** `/reactions/toggle`
- **Base URL:** `https://dev.to/api`
- **Official documentation:** [Toggle Reaction](https://developers.forem.com/api/v1#tag/reactions/paths/~1reactions~1toggle/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `list` | yes | Reaction category: like, unicorn, exploding_head, raised_hands, or fire. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `reactable_id` | query | `number` | yes | ID of the article, comment, or user to react to. |
| `reactable_type` | query | `list` | yes | Reactable type: Article, Comment, or User. Accepted values: `0`, `1`, `2`. |
