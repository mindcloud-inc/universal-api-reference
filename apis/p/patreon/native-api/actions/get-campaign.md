# Get Campaign with Patreon

Retrieves a campaign by ID from Patreon.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaignId`
- **Base URL:** `https://www.patreon.com/api/oauth2/v2`
- **Official documentation:** [Get Campaign](https://docs.patreon.com#get-api-oauth2-v2-campaigns-campaign_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The Patreon campaign ID. |
