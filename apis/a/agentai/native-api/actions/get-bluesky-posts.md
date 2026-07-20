# Get Bluesky Posts with Agent.ai

Retrieves Bluesky posts from Agent.ai by handle.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/get_bluesky_posts`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Get Bluesky Posts](https://docs.agent.ai/api-reference/get-data/get-bluesky-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | body | `string` | yes | Bluesky handle to fetch posts from. |
| `num_posts` | body | `number` | yes | Number of Bluesky posts to fetch. |
