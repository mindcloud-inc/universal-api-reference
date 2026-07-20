# Get Campaign Details with Moosend

Retrieves campaign details from Moosend.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/{{CampaignID}}/view.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Get Campaign Details](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54586-Get-campaign-details?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CampaignID` | path | `string` | yes | The ID of the campaign that contains the details you are requesting. |
