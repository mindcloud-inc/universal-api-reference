# Append Session Tags with Devin

Updates session tags by appending new tags in Devin.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/organizations/:org_id/sessions/:devin_id/tags`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Append Session Tags](https://docs.devin.ai/api-reference/v3/sessions/post-organizations-session-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `devin_id` | path | `string` | yes | Session ID prefixed with devin-. |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `tags[]` | body | `array<string>` | yes | Tags to append to the session. |
