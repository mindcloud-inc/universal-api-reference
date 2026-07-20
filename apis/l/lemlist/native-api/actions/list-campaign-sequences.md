# List Campaign Sequences with lemlist

Retrieves sequences from a lemlist campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/:campaignId/sequences`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [List Campaign Sequences](https://developer.lemlist.com/api-reference/endpoints/sequences/get-campaign-sequences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The ID of the campaign whose sequences should be retrieved. |
