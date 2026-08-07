# Update Campaign Budget with Google Ads

Updates an existing campaign budget in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/campaignBudgets:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Update Campaign Budget](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignBudgetService/MutateCampaignBudgets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[].update.amountMicros` | body | `number` | no | — |
| `operations[].update.resourceName` | body | `string` | yes | — |
| `operations[].updateMask` | body | `string` | no | — |
| `partialFailure` | body | `boolean` | no | — |
| `responseContentType` | body | `list` | no | Accepted values: `MUTABLE_RESOURCE`, `RESOURCE_NAME_ONLY`, `UNSPECIFIED`. |
| `validateOnly` | body | `boolean` | no | — |
