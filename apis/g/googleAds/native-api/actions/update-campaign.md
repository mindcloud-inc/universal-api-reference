# Update Campaign with Google Ads

Updates an existing campaign in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/campaigns:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Update Campaign](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignService/MutateCampaigns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | — |
| `operations[]` | body | `array<object>` | yes | List of mutate operations. |
| `operations[].update` | body | `object` | no | Update payload for each mutate operation. |
| `operations[].update.name` | body | `string` | no | — |
| `operations[].update.resourceName` | body | `string` | yes | — |
| `operations[].update.status` | body | `list` | no | Accepted values: `ENABLED`, `PAUSED`, `REMOVED`, `UNKNOWN`, `UNSPECIFIED`. |
| `operations[].updateMask` | body | `string` | no | — |
| `partialFailure` | body | `boolean` | no | — |
| `responseContentType` | body | `list` | no | Accepted values: `MUTABLE_RESOURCE`, `RESOURCE_NAME_ONLY`, `UNSPECIFIED`. |
| `validateOnly` | body | `boolean` | no | — |
