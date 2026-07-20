# Run Campaign with Woodpecker.co

Starts an existing campaign in Woodpecker.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/campaigns/[:campaign_id]/run`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [Run Campaign](https://developers.woodpecker.co/docs/campaigns/POST-run-campaign/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID from Woodpecker. |
