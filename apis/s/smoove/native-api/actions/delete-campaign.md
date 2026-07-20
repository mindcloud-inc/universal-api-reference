# Delete Campaign with Smoove

Deletes an existing email campaign from Smoove.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/Campaigns/:id`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [Delete Campaign](https://rest.smoove.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `by` | query | `list` | no | Accepted values: `CampaignId`, `ExternalId`. |
