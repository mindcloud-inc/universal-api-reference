# Add Negative Campaign Keyword with Google Ads

Creates a negative campaign keyword in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/campaignCriteria:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Add Negative Campaign Keyword](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignCriterionService/MutateCampaignCriteria)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[].create.campaign` | body | `string` | yes | — |
| `operations[].create.keyword.matchType` | body | `list` | yes | Accepted values: `BROAD`, `EXACT`, `PHRASE`, `UNKNOWN`, `UNSPECIFIED`. |
| `operations[].create.keyword.text` | body | `string` | yes | — |
| `partialFailure` | body | `boolean` | no | — |
| `responseContentType` | body | `list` | no | Accepted values: `MUTABLE_RESOURCE`, `RESOURCE_NAME_ONLY`, `UNSPECIFIED`. |
| `validateOnly` | body | `boolean` | no | — |
| `operations[]` | body | `array<object>` | yes | — |
| `operations[].create` | body | `object` | no | — |
| `operations[].create.keyword` | body | `object` | no | — |
