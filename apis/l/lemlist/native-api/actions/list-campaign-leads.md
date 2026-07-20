# List Campaign Leads with lemlist

Retrieves leads from a lemlist campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaignId/leads/`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [List Campaign Leads](https://developer.lemlist.com/api-reference/endpoints/leads/get-campaign-leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The ID of the campaign to retrieve leads from. |
| `state` | query | `string` | no | Filter leads by their current state. |
