# List Campaign Donations with Charidy

Retrieves donations for a campaign from Charidy.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/campaign/:campaignId/donations`
- **Base URL:** `https://api.charidy.com`
- **Official documentation:** [List Campaign Donations](https://documenter.getpostman.com/view/1118680/S1a4WS4g)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `number` | yes | The campaign ID whose donations to list. |
| `sortBy` | query | `string` | no | Sort donations by the requested field and direction. |
| `limit` | query | `number` | no | Maximum number of donations to return. |
| `fromDonationID` | query | `number` | no | Return donations made after this donation ID. |
