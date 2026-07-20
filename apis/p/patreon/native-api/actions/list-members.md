# List Members with Patreon

Retrieves members for a Patreon campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaignId/members`
- **Base URL:** `https://www.patreon.com/api/oauth2/v2`
- **Official documentation:** [List Members](https://docs.patreon.com#get-api-oauth2-v2-campaigns-campaign_id-members)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The Patreon campaign ID. |
