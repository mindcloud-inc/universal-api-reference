# Add Leads To Campaign with Hey Reach

Adds leads to a campaign in Hey Reach.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/campaign/AddLeadsToCampaignV2`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [Add Leads To Campaign](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | body | `number` | yes |
| `accountLeadPairs[]` | body | `array<object>` | yes |
| `resumeFinishedCampaign` | body | `boolean` | no |
| `resumePausedCampaign` | body | `boolean` | no |
