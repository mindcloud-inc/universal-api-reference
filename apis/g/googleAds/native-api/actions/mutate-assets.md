# Mutate Assets with Google Ads

Creates, updates, or removes assets in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/assets:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Mutate Assets](https://developers.google.com/google-ads/api/reference/rpc/v22/AssetService/MutateAssets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `operations[]` | body | `array<object>` | yes | Mutation operations array for assets. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
