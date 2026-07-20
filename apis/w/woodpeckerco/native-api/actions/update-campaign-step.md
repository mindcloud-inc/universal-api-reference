# Update Campaign Step with Woodpecker.co

Updates delivery times for a Woodpecker campaign step.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/v2/campaigns/[:campaign_id]/steps/[:step_id]`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [Update Campaign Step](https://developers.woodpecker.co/docs/campaigns/PATCH-campaign-step/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID from Woodpecker. |
| `step_id` | path | `number` | yes | Step ID from Woodpecker. |
