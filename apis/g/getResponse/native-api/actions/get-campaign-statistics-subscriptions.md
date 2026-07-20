# Get Campaign Statistics Subscriptions with GetResponse

Retrieves subscription counts and origins for GetResponse campaigns.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/statistics/subscriptions`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Get Campaign Statistics Subscriptions](https://apireference.getresponse.com/#operation/getCampaignStatisticsSubscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[campaignId]` | query | `string` | yes | Campaign identifier for statistics lookup |
| `query[groupBy]` | query | `string` | no | Group subscription statistics by interval |
| `query[createdOn][from]` | query | `string` | no | Start date for statistics window |
| `query[createdOn][to]` | query | `string` | no | End date for statistics window |
