# Send Campaign with Moosend

Sends a campaign in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/{{CampaignID}}/send.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Send Campaign](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54595-Send-a-campaign?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CampaignID` | path | `string` | yes | The ID of the draft campaign that you want to send. |
