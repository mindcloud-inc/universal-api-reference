# Send Session Message with Devin

Creates a session message in Devin.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/organizations/:org_id/sessions/:devin_id/messages`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Send Session Message](https://docs.devin.ai/api-reference/v3/sessions/post-organizations-session-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `devin_id` | path | `string` | yes | Session ID prefixed with devin-. |
| `message` | body | `string` | yes | Message to send to the active Devin session. |
| `org_id` | path | `string` | yes | Devin organization ID. |
