# Generate Ad Group Themes with Google Ads

Generates ad group themes in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId:generateAdGroupThemes`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Generate Ad Group Themes](https://developers.google.com/google-ads/api/reference/rpc/v22/KeywordPlanIdeaService/GenerateAdGroupThemes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID to generate ad group themes for (without dashes). |
| `keywords[]` | body | `array<string>` | yes | Seed keywords to group into themes. |
| `adGroups[]` | body | `array<string>` | yes | Ad group names for thematic grouping. |
