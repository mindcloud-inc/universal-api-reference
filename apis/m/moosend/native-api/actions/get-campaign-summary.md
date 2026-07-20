# Get Campaign Summary with Moosend

Retrieves campaign summary from Moosend.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/{{CampaignID}}/view-summary.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Get Campaign Summary](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54604-Get-campaign-summary?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CampaignID` | path | `string` | yes | The ID of the campaign that you want to get a summary of. |
