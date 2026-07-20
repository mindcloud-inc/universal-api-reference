# Schedule Campaign with Zoho Campaigns

Schedules a campaign in Zoho Campaigns.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendcampaign`
- **Base URL:** `https://campaigns.zoho.com/api/v1.1`
- **Official documentation:** [Schedule Campaign](https://www.zoho.com/campaigns/help/developers/schedule-campaign.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignkey` | query | `string` | yes | Campaign key from a recent-campaign response. |
| `scheduledate` | query | `string` | yes | Date to schedule the campaign in mm/dd/yyyy format. |
| `schedulehour` | query | `number` | yes | Hour portion of the scheduled send time. |
| `scheduleminute` | query | `number` | yes | Minute portion of the scheduled send time. |
| `am_pm` | query | `string` | yes | Meridiem for the scheduled send time. Accepted values: `0`, `1`. |
| `istimewarp` | query | `boolean` | no | Whether to send in the sender's time zone. |
| `sendingTZ` | query | `string` | no | Recipient time zone for scheduled sending. |
