# Get Newsletter Statistics with GetResponse

Retrieves total newsletter statistics from GetResponse.

## Endpoint

- **Method:** `GET`
- **Path:** `/newsletters/statistics`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Get Newsletter Statistics](https://apireference.getresponse.com/#operation/getNewsletterStatisticsCollection)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query[campaignId]` | query | `string` | no | Campaign identifier for statistics lookup |
| `query[newsletterId]` | query | `string` | no | Newsletter identifier for statistics lookup |
| `query[groupBy]` | query | `string` | no | Group newsletter statistics by interval |
| `query[createdOn][from]` | query | `string` | no | Start date for statistics window |
| `query[createdOn][to]` | query | `string` | no | End date for statistics window |
