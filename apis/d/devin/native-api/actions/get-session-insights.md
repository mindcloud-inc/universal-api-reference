# Get Session Insights with Devin

Retrieves generated session insights from Devin.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/organizations/:org_id/sessions/:devin_id/insights`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Get Session Insights](https://docs.devin.ai/api-reference/v3/sessions/get-organizations-session-insights)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `devin_id` | path | `string` | yes | Session ID prefixed with devin-. |
| `org_id` | path | `string` | yes | Devin organization ID. |
