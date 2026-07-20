# Get Instagram Followers with Agent.ai

Retrieves Instagram followers from Agent.ai by username.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/get_instagram_followers`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Get Instagram Followers](https://docs.agent.ai/api-reference/get-data/get-instagram-followers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | Instagram username without @. |
| `limit` | body | `string` | yes | Number of top followers to retrieve. |
