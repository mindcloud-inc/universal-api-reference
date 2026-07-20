# Search Campaigns with LinkedIn Ads Reports

Finds campaigns in LinkedIn Ads Reports.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/adAccounts/{{adAccountId}}/adCampaigns`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Search Campaigns](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-campaigns?view=li-lms-2026-04)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | LinkedIn numeric ad account ID. |
