# Get Search Results with Agent.ai

Finds Google or YouTube results in Agent.ai by query.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/get_search_results`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Get Search Results](https://docs.agent.ai/api-reference/get-data/search-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_engine` | body | `string` | yes | Search engine to use. |
| `query` | body | `string` | yes | Search terms to find specific results. |
| `num_posts` | body | `number` | yes | Number of results to return. |
