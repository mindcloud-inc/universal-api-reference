# Pause Campaign with Google Ads

Updates a campaign to paused status in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/campaigns:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Pause Campaign](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignService/MutateCampaigns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[]` | body | `array<object>` | no | List of mutate operations. |
| `operations[].update` | body | `object` | no | Update payload for each mutate operation. |
| `operations[].update.resourceName` | body | `string` | yes | — |
| `partialFailure` | body | `boolean` | no | — |
| `responseContentType` | body | `list` | no | Accepted values: `MUTABLE_RESOURCE`, `RESOURCE_NAME_ONLY`, `UNSPECIFIED`. |
| `validateOnly` | body | `boolean` | no | — |
