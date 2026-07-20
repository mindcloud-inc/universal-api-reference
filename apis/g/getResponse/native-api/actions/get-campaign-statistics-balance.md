# Get Campaign Statistics Balance with GetResponse

Retrieves balance statistics for GetResponse campaigns.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/statistics/balance`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Get Campaign Statistics Balance](https://apireference.getresponse.com/#operation/getCampaignStatisticsBalance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[campaignId]` | query | `string` | yes | Campaign identifier for statistics lookup |
| `query[groupBy]` | query | `string` | no | Group balance statistics by interval |
| `query[createdOn][from]` | query | `string` | no | Start date for statistics window |
| `query[createdOn][to]` | query | `string` | no | End date for statistics window |
