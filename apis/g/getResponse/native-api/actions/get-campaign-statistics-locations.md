# Get Campaign Statistics Locations with GetResponse

Retrieves subscriber location statistics for GetResponse campaigns.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/statistics/locations`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Get Campaign Statistics Locations](https://apireference.getresponse.com/#operation/getCampaignStatisticsLocations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[campaignId]` | query | `string` | yes | Campaign identifier for statistics lookup |
| `query[groupBy]` | query | `string` | no | Group location statistics by interval |
| `query[createdOn][from]` | query | `string` | no | Start date for statistics window |
| `query[createdOn][to]` | query | `string` | no | End date for statistics window |
