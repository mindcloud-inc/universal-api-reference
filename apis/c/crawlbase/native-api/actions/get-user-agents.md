# Get User Agents with Crawlbase

Retrieves random user-agent strings from Crawlbase.

## Endpoint

- **Method:** `GET`
- **Path:** `/user_agents`
- **Base URL:** `https://api.crawlbase.com`
- **Official documentation:** [Get User Agents](https://crawlbase.com/docs/user-agents-api/parameters/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device` | query | `list` | no | Optional device category for random user agents: desktop or mobile. Accepted values: `0`, `1`. |
| `size` | query | `number` | no | Optional number of user agents to return. Crawlbase documents a maximum of 10 and default of 1. |
