# Get Recent Tweets with Agent.ai

Retrieves recent tweets from Agent.ai by Twitter handle.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/get_recent_tweets`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Get Recent Tweets](https://docs.agent.ai/api-reference/get-data/get-recent-tweets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile_handle` | body | `string` | yes | Twitter handle to fetch recent tweets from. |
| `recent_tweets_count` | body | `string` | yes | Number of recent tweets to fetch. |
