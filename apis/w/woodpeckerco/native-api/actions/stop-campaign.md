# Stop Campaign with Woodpecker.co

Stops an existing campaign in Woodpecker.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/campaigns/[:campaign_id]/stop`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [Stop Campaign](https://developers.woodpecker.co/docs/campaigns/POST-stop-campaign/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID from Woodpecker. |
