# Attach Keyword Label with Google Ads

Attaches a label to a keyword criterion in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/adGroupCriterionLabels:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Attach Keyword Label](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupCriterionLabelService/MutateAdGroupCriterionLabels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[]` | body | `array<object>` | no | List of mutate operations. |
| `operations[].create` | body | `object` | no | Create payload for each mutate operation. |
| `operations[].create.adGroupCriterion` | body | `string` | yes | — |
| `operations[].create.label` | body | `string` | yes | — |
| `partialFailure` | body | `boolean` | no | — |
| `validateOnly` | body | `boolean` | no | — |
