# Mutate Conversion Actions with Google Ads

Creates, updates, or removes conversion actions in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/conversionActions:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Mutate Conversion Actions](https://developers.google.com/google-ads/api/reference/rpc/v22/ConversionActionService/MutateConversionActions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `operations[]` | body | `array<object>` | yes | Mutation operations array for conversion actions. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
