# Create or Update Tool with OnceOnly

Creates or updates a tool in OnceOnly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tools`
- **Base URL:** `https://api.onceonly.tech`
- **Official documentation:** [Create or Update Tool](https://docs.onceonly.tech/reference/tools/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Tool name. |
| `scope_id` | body | `string` | yes | Tool scope, such as global or agent:agent_id. |
| `url` | body | `string` | yes | Tool endpoint URL. |
| `auth` | body | `object` | yes | Auth object. Set type to hmac_sha256 and include secret. |
| `timeout_ms` | body | `number` | no | Request timeout in milliseconds. |
| `max_retries` | body | `number` | no | Retry count. |
| `enabled` | body | `boolean` | no | Whether the tool is enabled. |
| `description` | body | `string` | no | Optional tool description. |
