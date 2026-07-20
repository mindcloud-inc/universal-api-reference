# Get LinkedIn Activity with Agent.ai

Retrieves LinkedIn posts from Agent.ai by profile URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/get_linkedin_activity`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Get LinkedIn Activity](https://docs.agent.ai/api-reference/get-data/get-linkedin-activity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile_urls` | body | `string` | yes | LinkedIn profile URLs, one per line. |
| `num_posts` | body | `number` | yes | Number of recent posts to fetch from each profile. |
