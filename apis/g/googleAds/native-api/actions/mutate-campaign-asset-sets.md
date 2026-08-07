# Mutate Campaign Asset Sets with Google Ads

Creates, updates, or removes campaign asset sets in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/campaignAssetSets:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Mutate Campaign Asset Sets](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignAssetSetService/MutateCampaignAssetSets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `operations[]` | body | `array<object>` | yes | Mutation operations array for campaign asset sets. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
