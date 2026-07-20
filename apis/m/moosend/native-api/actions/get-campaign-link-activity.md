# Get Campaign Link Activity with Moosend

Retrieves campaign link activity from Moosend.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/{{CampaignID}}/stats/links.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Get Campaign Link Activity](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54606-Get-campaign-link-activity?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CampaignID` | path | `string` | yes | The ID of the campaign that you want to get link activity by location of. |
