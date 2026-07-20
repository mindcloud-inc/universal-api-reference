# Get Campaign Statistics with Smoove

Retrieves aggregated statistics for a Smoove email campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/Campaigns/:id/Statistics`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [Get Campaign Statistics](https://rest.smoove.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `by` | query | `list` | no | Accepted values: `CampaignId`, `ExternalId`. |
