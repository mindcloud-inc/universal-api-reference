# Mutate Conversion Custom Variables with Google Ads

Creates, updates, or removes conversion custom variables in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/conversionCustomVariables:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Mutate Conversion Custom Variables](https://developers.google.com/google-ads/api/reference/rpc/v22/ConversionCustomVariableService/MutateConversionCustomVariables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `operations[]` | body | `array<object>` | yes | Mutation operations array for conversion custom variables. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
