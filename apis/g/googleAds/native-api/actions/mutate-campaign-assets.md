# Mutate Campaign Assets with Google Ads

Creates, updates, or removes campaign assets in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/campaignAssets:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Mutate Campaign Assets](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignAssetService/MutateCampaignAssets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `operations[]` | body | `array<object>` | yes | Mutation operations array for campaign assets. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
