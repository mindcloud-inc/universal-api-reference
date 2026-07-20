# Create Remote Browser Session with AgentQL

Creates a remote browser session with CDP access in AgentQL.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tetra/sessions`
- **Base URL:** `https://api.agentql.com`
- **Official documentation:** [Create Remote Browser Session](https://docs.agentql.com/rest-api/api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `browser_ua_preset` | body | `string` | no |
| `browser_profile` | body | `string` | no |
| `shutdown_mode` | body | `string` | no |
| `inactivity_timeout_seconds` | body | `number` | no |
| `sub_user_id` | body | `string` | no |
| `proxy` | body | `object` | no |
| `type` | body | `string` | no |
| `country_code` | body | `string` | no |
| `url` | body | `string` | no |
| `username` | body | `string` | no |
