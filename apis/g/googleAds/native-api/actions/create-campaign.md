# Create Campaign with Google Ads

Creates a campaign in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/campaigns:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Create Campaign](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignService/MutateCampaigns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID where the campaign will be created (without dashes). |
| `operations[].create` | body | `object` | no | — |
| `operations[].create.manualCpc` | body | `object` | no | — |
| `operations[].create.name` | body | `string` | yes | — |
| `operations[].create.networkSettings.targetGoogleSearch` | body | `boolean` | no | Format: `toggle`. |
| `partialFailure` | body | `boolean` | no | — |
| `responseContentType` | body | `list` | no | Accepted values: `MUTABLE_RESOURCE`, `RESOURCE_NAME_ONLY`, `UNSPECIFIED`. |
| `validateOnly` | body | `boolean` | no | — |
| `operations[]` | body | `array<object>` | yes | — |
| `operations[].create.campaignBudget` | body | `string` | yes | — |
| `operations[].create.networkSettings.targetSearchNetwork` | body | `boolean` | no | Format: `toggle`. |
| `operations[].create.advertisingChannelType` | body | `list` | yes | Accepted values: `DISPLAY`, `PERFORMANCE_MAX`, `SEARCH`, `SHOPPING`, `VIDEO`. |
| `operations[].create.networkSettings.targetContentNetwork` | body | `boolean` | no | Format: `toggle`. |
| `operations[].create.networkSettings.targetPartnerSearchNetwork` | body | `boolean` | no | Format: `toggle`. |
| `operations[].create.status` | body | `list` | no | Accepted values: `ENABLED`, `PAUSED`. |
| `operations[].create.networkSettings` | body | `object` | no | — |
| `operations[].create.containsEuPoliticalAdvertising` | body | `list` | no | Accepted values: `CONTAINS_EU_POLITICAL_ADVERTISING`, `DOES_NOT_CONTAIN_EU_POLITICAL_ADVERTISING`, `UNKNOWN`, `UNSPECIFIED`. Format: `toggle`. |
