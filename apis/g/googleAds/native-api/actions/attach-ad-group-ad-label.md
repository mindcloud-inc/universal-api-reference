# Attach Ad Group Ad Label with Google Ads

Attaches a label to an ad group ad in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/adGroupAdLabels:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Attach Ad Group Ad Label](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAdLabelService/MutateAdGroupAdLabels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[]` | body | `array<object>` | no | List of mutate operations. |
| `operations[].create` | body | `object` | no | Create payload for each mutate operation. |
| `operations[].create.adGroupAd` | body | `string` | yes | — |
| `operations[].create.label` | body | `string` | yes | — |
| `partialFailure` | body | `boolean` | no | — |
| `validateOnly` | body | `boolean` | no | — |
