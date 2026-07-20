# Get Campaign Statistics Removals with GetResponse

Retrieves removal statistics for GetResponse campaigns.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/statistics/removals`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Get Campaign Statistics Removals](https://apireference.getresponse.com/#operation/getCampaignStatisticsRemovals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[campaignId]` | query | `string` | yes | Campaign identifier for statistics lookup |
| `query[groupBy]` | query | `string` | no | Group removal statistics by interval |
| `query[createdOn][from]` | query | `string` | no | Start date for statistics window |
| `query[createdOn][to]` | query | `string` | no | End date for statistics window |
