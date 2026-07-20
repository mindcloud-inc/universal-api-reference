# Get Campaign Stats with lemlist

Retrieves statistics for a lemlist campaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/campaigns/:campaignId/stats`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [Get Campaign Stats](https://developer.lemlist.com/api-reference/endpoints/campaigns/get-campaign-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The ID of the campaign to inspect. |
| `startDate` | query | `string` | yes | The start of the reporting range in ISO 8601 format. |
| `endDate` | query | `string` | yes | The end of the reporting range in ISO 8601 format. |
| `sendUser` | query | `string` | no | Filter statistics to a specific sending user. |
| `ABSelected` | query | `list` | no | Return statistics for only the A or B branch. Accepted values: `A`, `B`. |
| `channels` | query | `string` | no | A JSON array string of channels to include. |
