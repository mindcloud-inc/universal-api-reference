# Retrieve Viber Trackings by Campaign with Routee

Retrieves Viber trackings by campaign from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/viber/tracking/campaign/:campaignTrackingId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve Viber Trackings by Campaign](https://docs.routee.net/reference/retrieve-viber-tracking-by-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | query | `number` | no | The number of items to retrieve, default value is 20. |
| `sort` | query | `number` | no | The field name that will be used to sort the results. |
| `campaignTrackingId` | path | `string` | yes | The tracking id of the viber campaign which includes the messages. |
