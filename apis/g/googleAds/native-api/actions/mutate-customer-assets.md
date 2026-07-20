# Mutate Customer Assets with Google Ads

Creates, updates, or removes customer assets in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/customerAssets:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Mutate Customer Assets](https://developers.google.com/google-ads/api/reference/rpc/v22/CustomerAssetService/MutateCustomerAssets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `operations[]` | body | `array<object>` | yes | Mutation operations array for customer assets. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
