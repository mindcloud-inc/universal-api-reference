# Send Campaign with Smoove

Sends a saved email campaign in Smoove.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/Campaigns/:id/Send`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [Send Campaign](https://rest.smoove.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `by` | query | `list` | no | Accepted values: `CampaignId`, `ExternalId`. |
| `scheduleTo` | query | `string` | no | — |
