# Get Twitter Users with Agent.ai

Finds Twitter user profiles in Agent.ai by keywords.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/get_twitter_users`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Get Twitter Users](https://docs.agent.ai/api-reference/get-data/get-twitter-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keywords` | body | `string` | yes | Keywords to find relevant Twitter users. |
| `num_users` | body | `number` | yes | Number of user profiles to retrieve. |
