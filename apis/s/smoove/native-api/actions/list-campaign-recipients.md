# List Campaign Recipients with Smoove

Retrieves recipient responses for a Smoove email campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/Campaigns/:id/Recipients`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [List Campaign Recipients](https://rest.smoove.io)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `by` | query | `list` | no | Accepted values: `CampaignId`, `ExternalId`. |
