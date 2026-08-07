# Mutate Ad Group Assets with Google Ads

Creates, updates, or removes ad group assets in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/adGroupAssets:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Mutate Ad Group Assets](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAssetService/MutateAdGroupAssets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `operations[]` | body | `array<object>` | yes | Mutation operations array for ad group assets. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
