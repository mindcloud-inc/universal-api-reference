# Mutate Asset Set Assets with Google Ads

Creates, updates, or removes asset set assets in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/assetSetAssets:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Mutate Asset Set Assets](https://developers.google.com/google-ads/api/reference/rpc/v22/AssetSetAssetService/MutateAssetSetAssets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `operations[]` | body | `array<object>` | yes | Mutation operations array for asset set assets. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
