# Get Creative with LinkedIn Ads Reports

Retrieves a creative from LinkedIn Ads Reports.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/adAccounts/{{adAccountId}}/creatives/{{creativeId}}`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Get Creative](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-creatives?view=li-lms-2026-04)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | LinkedIn numeric ad account ID. |
| `creativeId` | path | `string` | yes | LinkedIn numeric creative ID. |
