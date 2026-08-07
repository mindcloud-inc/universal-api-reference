# Attach Ad Group Label with Google Ads

Attaches a label to an ad group in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/adGroupLabels:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Attach Ad Group Label](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupLabelService/MutateAdGroupLabels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[]` | body | `array<object>` | no | List of mutate operations. |
| `operations[].create` | body | `object` | no | Create payload for each mutate operation. |
| `operations[].create.adGroup` | body | `string` | yes | — |
| `operations[].create.label` | body | `string` | yes | — |
| `partialFailure` | body | `boolean` | no | — |
| `validateOnly` | body | `boolean` | no | — |
