# Create Ad Group with Google Ads

Creates an ad group in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/adGroups:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Create Ad Group](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupService/MutateAdGroups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID where the ad group will be created (without dashes). |
| `operations[].create` | body | `object` | no | — |
| `operations[].create.name` | body | `string` | no | — |
| `operations[]` | body | `array` | no | — |
| `operations[].create.campaign` | body | `string` | yes | Campaign resource name for the ad group, format customers/{customer_id}/campaigns/{campaign_id}. |
| `operations[].create.status` | body | `string` | no | — |
| `operations[].create.cpcBidMicros` | body | `number` | no | — |
| `operations[].create.period` | body | `string` | no | — |
| `operations[].create.startDate` | body | `string` | no | — |
| `operations[].create.endDate` | body | `string` | no | — |
