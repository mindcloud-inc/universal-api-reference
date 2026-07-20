# Get Campaign Statistics Origins with GetResponse

Retrieves subscriber origin statistics for GetResponse campaigns.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/statistics/origins`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Get Campaign Statistics Origins](https://apireference.getresponse.com/#operation/getCampaignStatisticsOrigins)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[campaignId]` | query | `string` | yes | Campaign identifier for statistics lookup |
| `query[groupBy]` | query | `string` | no | Group origin statistics by interval |
| `query[createdOn][from]` | query | `string` | no | Start date for statistics window |
| `query[createdOn][to]` | query | `string` | no | End date for statistics window |
