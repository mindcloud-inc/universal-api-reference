# Pause Campaign with Woodpecker.co

Pauses an active campaign in Woodpecker.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/campaigns/[:campaign_id]/pause`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [Pause Campaign](https://developers.woodpecker.co/docs/campaigns/POST-pause-campaign/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID from Woodpecker. |
