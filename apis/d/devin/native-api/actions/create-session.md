# Create Session with Devin

Creates a new session in Devin.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/organizations/:org_id/sessions`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Create Session](https://docs.devin.ai/api-reference/v3/sessions/post-organizations-sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `prompt` | body | `string` | yes | Prompt for the new Devin session. |
| `title` | body | `string` | no | Optional title for the session. |
