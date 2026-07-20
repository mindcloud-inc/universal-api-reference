# Add Keyword Criterion with Google Ads

Creates a keyword criterion in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/adGroupCriteria:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Add Keyword Criterion](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupCriterionService/MutateAdGroupCriteria)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[].create.adGroup` | body | `string` | yes | — |
| `operations[].create.cpcBidMicros` | body | `number` | no | — |
| `operations[].create.keyword.matchType` | body | `list` | yes | Accepted values: `BROAD`, `EXACT`, `PHRASE`, `UNKNOWN`, `UNSPECIFIED`. |
| `operations[].create.keyword.text` | body | `string` | yes | — |
| `operations[].create.status` | body | `list` | no | Accepted values: `ENABLED`, `PAUSED`, `REMOVED`, `UNKNOWN`, `UNSPECIFIED`. |
| `partialFailure` | body | `boolean` | no | — |
| `responseContentType` | body | `list` | no | Accepted values: `MUTABLE_RESOURCE`, `RESOURCE_NAME_ONLY`, `UNSPECIFIED`. |
| `validateOnly` | body | `boolean` | no | — |
| `operations[]` | body | `array<object>` | yes | — |
| `operations[].create` | body | `object` | no | — |
| `operations[].create.keyword` | body | `object` | no | — |
