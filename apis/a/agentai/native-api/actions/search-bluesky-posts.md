# Search Bluesky Posts with Agent.ai

Finds Bluesky posts in Agent.ai by query.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/search_bluesky_posts`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Search Bluesky Posts](https://docs.agent.ai/api-reference/get-data/search-bluesky-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Text query to search Bluesky posts. |
| `num_posts` | body | `number` | yes | Number of Bluesky posts to return. |
