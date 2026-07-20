# List Session Messages with Devin

Retrieves session messages from a Devin session.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/organizations/:org_id/sessions/:devin_id/messages`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [List Session Messages](https://docs.devin.ai/api-reference/v3/sessions/get-organizations-session-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `devin_id` | path | `string` | yes | Session ID prefixed with devin-. |
| `org_id` | path | `string` | yes | Devin organization ID. |
