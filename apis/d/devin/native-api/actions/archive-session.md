# Archive Session with Devin

Archives an existing session in Devin.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/organizations/:org_id/sessions/:devin_id/archive`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Archive Session](https://docs.devin.ai/api-reference/v3/sessions/post-organizations-session-archive)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `devin_id` | path | `string` | yes | Session ID prefixed with devin-. |
| `org_id` | path | `string` | yes | Devin organization ID. |
