# Get Campaign with LinkedIn Ads Reports

Retrieves a campaign from LinkedIn Ads Reports.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/adAccounts/{{adAccountId}}/adCampaigns/{{campaignId}}`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Get Campaign](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-campaigns?view=li-lms-2026-04)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | LinkedIn numeric ad account ID. |
| `campaignId` | path | `string` | yes | LinkedIn numeric sponsored campaign ID. |
