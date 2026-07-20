# Pause Campaign with Dynosend

Pauses a campaign in Dynosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/pause`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Pause Campaign](https://developers.dynosend.com/#pauseacampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_uid` | body | `string` | yes | The UID of the campaign to pause. |
