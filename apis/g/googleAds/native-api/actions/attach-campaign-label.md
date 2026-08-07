# Attach Campaign Label with Google Ads

Attaches a label to a campaign in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/campaignLabels:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Attach Campaign Label](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignLabelService/MutateCampaignLabels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[]` | body | `array<object>` | no | List of mutate operations. |
| `operations[].create` | body | `object` | no | Create payload for each mutate operation. |
| `operations[].create.campaign` | body | `string` | yes | — |
| `operations[].create.label` | body | `string` | yes | — |
| `partialFailure` | body | `boolean` | no | — |
| `validateOnly` | body | `boolean` | no | — |
