# Search Creatives with LinkedIn Ads Reports

Finds creatives in LinkedIn Ads Reports.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/adAccounts/{{adAccountId}}/creatives`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Search Creatives](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-creatives?view=li-lms-2026-04)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | LinkedIn numeric ad account ID. |
