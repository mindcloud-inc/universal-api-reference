# Unschedule Campaign with Moosend

Unschedules a campaign in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/{{CampaignID}}/unschedule.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Unschedule Campaign](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54608-Unschedule-a-campaign?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CampaignID` | path | `string` | yes | The ID of the campaign that you want to unschedule. |
