# Get Campaign Resources with SuperMCP

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp/campaign_and_resource_get`
- **Base URL:** `https://mcp.supermetrics.com`
- **Official documentation:** [Get Campaign Resources](https://mcp.supermetrics.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ds_id` | body | `string` | yes | Ad platform data source code: AW, FA, AC, TIK, or LIA. |
| `account_id` | body | `string` | yes | Platform ad account ID from Discover Accounts. |
| `resource_type` | body | `string` | no | Resource to query: campaigns, health_check, assets, pages, posts, keyword_ideas, keyword_volumes, targeting_search, reach_estimate, audiences, recommendations, history, or conversions. |
| `params` | body | `object` | no | Resource-type-specific parameters as documented by Supermetrics. |
| `max_rows` | body | `number` | no | Maximum resources to return. |
