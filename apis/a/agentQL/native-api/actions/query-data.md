# Query Data with AgentQL

Queries structured data from web pages with AgentQL.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/query-data`
- **Base URL:** `https://api.agentql.com`
- **Official documentation:** [Query Data](https://docs.agentql.com/rest-api/api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | body | `string` | no |
| `prompt` | body | `string` | no |
| `url` | body | `string` | no |
| `html` | body | `string` | no |
| `params` | body | `object` | no |
| `wait_for` | body | `number` | no |
| `is_scroll_to_bottom_enabled` | body | `boolean` | no |
| `mode` | body | `string` | no |
| `is_screenshot_enabled` | body | `boolean` | no |
| `browser_profile` | body | `string` | no |
| `proxy` | body | `object` | no |
| `type` | body | `string` | no |
| `country_code` | body | `string` | no |
| `url` | body | `string` | no |
| `username` | body | `string` | no |
