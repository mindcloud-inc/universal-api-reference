# Get Campaign Group with LinkedIn Ads Reports

Retrieves a campaign group from LinkedIn Ads Reports.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/adAccounts/{{adAccountId}}/adCampaignGroups/{{campaignGroupId}}`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Get Campaign Group](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-campaign-groups?view=li-lms-2026-04)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | LinkedIn numeric ad account ID. |
| `campaignGroupId` | path | `string` | yes | LinkedIn numeric sponsored campaign group ID. |
