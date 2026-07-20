# Edit Campaign with Woodpecker.co

Makes a Woodpecker campaign editable for changes.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/campaigns/[:campaign_id]/make_editable`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [Edit Campaign](https://developers.woodpecker.co/docs/campaigns/POST-editable-campaign/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `number` | yes | Campaign ID from Woodpecker. |
