# Track multiple messages for a specific bulk send out - campaign with Routee

Tracks multiple messages for a specific bulk send out - campaign in Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/sms/tracking/campaign/:campaignTrackingId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Track multiple messages for a specific bulk send out - campaign](https://docs.routee.net/reference/track-multiple-sms-of-a-specific-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignTrackingId` | path | `string` | yes | The tracking id of the campaign which includes the messages. |
| `page` | query | `string` | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | query | `string` | no | The number of items to retrieve, default value is 20. Max value is 2000. |
| `sort` | query | `string` | no | The field name that will be used to sort the results. |
