# Detach Ad Group Label with Google Ads

Detaches a label from an ad group in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/adGroupLabels:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Detach Ad Group Label](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupLabelService/MutateAdGroupLabels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[]` | body | `array<object>` | yes | List of mutate operations. |
| `operations[].remove` | body | `string` | yes | — |
| `partialFailure` | body | `boolean` | no | — |
| `validateOnly` | body | `boolean` | no | — |
