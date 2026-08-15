# Create Campaign Budget with Google Ads

Creates a campaign budget in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/campaignBudgets:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Create Campaign Budget](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignBudgetService/MutateCampaignBudgets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID where the campaign budget will be created (without dashes). |
| `operations[].create` | body | `object` | no | — |
| `operations[].create.name` | body | `string` | no | — |
| `operations[]` | body | `array` | yes | — |
| `operations[].create.deliveryMethod` | body | `list` | yes | — |
| `operations[].create.amountMicros` | body | `number` | yes | — |
| `operations[].create.period` | body | `string` | no | — |
| `operations[].create.startDate` | body | `string` | no | — |
| `operations[].create.endDate` | body | `string` | no | — |
