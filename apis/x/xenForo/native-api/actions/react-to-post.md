# React To Post with XenForo

Creates a reaction on a post in XenForo.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/:id/react`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [React To Post](https://docs.xenforo.com/api/post-posts-id-react)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the post to react to. |
| `reaction_id` | body | `number` | yes | ID of the reaction to use. Use the current reaction ID to undo. |
