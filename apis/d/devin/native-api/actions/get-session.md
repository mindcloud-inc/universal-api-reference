# Get Session with Devin

Retrieves a session record from Devin.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/organizations/:org_id/sessions/:devin_id`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Get Session](https://docs.devin.ai/api-reference/v3/sessions/get-organizations-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `devin_id` | path | `string` | yes | Session ID prefixed with devin-. |
| `org_id` | path | `string` | yes | Devin organization ID. |
