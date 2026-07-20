# Retrieve Voice Trackings by Campaign with Routee

Retrieves voice trackings by campaign from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/voice/tracking/campaign/:campaignTrackingId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve Voice Trackings by Campaign](https://docs.routee.net/reference/retrieve-voice-tracking-by-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `string` | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | query | `string` | no | The number of items to retrieve, default value is 20. |
| `sort` | query | `string` | no | The field name that will be used to sort the results. |
| `campaignTrackingId` | path | `string` | yes | The tracking id of the campaign which includes the messages. |
