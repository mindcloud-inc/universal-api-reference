# Generate Session Insights with Devin

Generates session insights for a Devin session.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/organizations/:org_id/sessions/:devin_id/insights/generate`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Generate Session Insights](https://docs.devin.ai/api-reference/v3/sessions/post-organizations-session-insights-generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `devin_id` | path | `string` | yes | Session ID prefixed with devin-. |
| `org_id` | path | `string` | yes | Devin organization ID. |
