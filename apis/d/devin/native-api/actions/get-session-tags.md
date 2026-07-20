# Get Session Tags with Devin

Retrieves tags for a session in Devin.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/organizations/:org_id/sessions/:devin_id/tags`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Get Session Tags](https://docs.devin.ai/api-reference/v3/sessions/get-organizations-session-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `devin_id` | path | `string` | yes | Session ID prefixed with devin-. |
| `org_id` | path | `string` | yes | Devin organization ID. |
