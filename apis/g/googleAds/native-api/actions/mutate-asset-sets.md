# Mutate Asset Sets with Google Ads

Creates, updates, or removes asset sets in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/assetSets:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Mutate Asset Sets](https://developers.google.com/google-ads/api/reference/rpc/v22/AssetSetService/MutateAssetSets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `operations[]` | body | `array<object>` | yes | Mutation operations array for asset sets. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
