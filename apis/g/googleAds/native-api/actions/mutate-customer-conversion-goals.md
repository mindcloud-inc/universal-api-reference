# Mutate Customer Conversion Goals with Google Ads

Creates, updates, or removes customer conversion goals in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/customerConversionGoals:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Mutate Customer Conversion Goals](https://developers.google.com/google-ads/api/reference/rpc/v22/CustomerConversionGoalService/MutateCustomerConversionGoals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `operations[]` | body | `array<object>` | yes | Mutation operations array for customer conversion goals. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
