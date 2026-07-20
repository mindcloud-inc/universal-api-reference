# Detach Ad Group Ad Label with Google Ads

Detaches a label from an ad group ad in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/adGroupAdLabels:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Detach Ad Group Ad Label](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAdLabelService/MutateAdGroupAdLabels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[]` | body | `array<object>` | no | List of mutate operations. |
| `operations[].remove` | body | `string` | yes | — |
| `partialFailure` | body | `boolean` | no | — |
| `validateOnly` | body | `boolean` | no | — |
