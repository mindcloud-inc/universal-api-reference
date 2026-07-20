# Terminate Session with Devin

Deletes an existing session from Devin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/organizations/:org_id/sessions/:devin_id`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Terminate Session](https://docs.devin.ai/api-reference/v3/sessions/delete-organizations-sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `devin_id` | path | `string` | yes | Session ID prefixed with devin-. |
| `org_id` | path | `string` | yes | Devin organization ID. |
