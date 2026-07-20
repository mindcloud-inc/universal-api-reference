# Start Campaign with Ringg AI

Starts a campaign in Ringg AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign/start`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Start Campaign](https://docs.ringg.ai/api-reference/endpoint/campaign/start-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | yes | (Required) ID of the agent that will handle the calls. |
| `list_id` | body | `string` | yes | (Required) ID of the uploaded campaign contact list. |
| `from_numbers[]` | body | `array<string>` | yes | (Required) Array of phone numbers to use for outbound calls. |
