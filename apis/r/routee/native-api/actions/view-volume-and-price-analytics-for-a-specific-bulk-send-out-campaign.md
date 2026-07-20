# View Volume and Price Analytics for a specific bulk send out - campaign with Routee

Retrieves volume and price analytics for a specific bulk send out - campaign from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/my/volPrice/perCampaign`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [View Volume and Price Analytics for a specific bulk send out - campaign](https://docs.routee.net/reference/view-volume-and-price-analytics-for-a-specific-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offset` | query | `date` | yes | The time offset that the result will be calculated in ISO 8601. |
| `campaignId` | query | `string` | yes | The id of the campaign that the messages belong to. |
