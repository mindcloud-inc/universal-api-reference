# Search Campaign Groups with LinkedIn Ads Reports

Finds campaign groups in LinkedIn Ads Reports.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/adAccounts/{{adAccountId}}/adCampaignGroups`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Search Campaign Groups](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-campaign-groups?view=li-lms-2026-04)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | LinkedIn numeric ad account ID. |
