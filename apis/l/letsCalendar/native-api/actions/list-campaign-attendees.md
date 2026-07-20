# List Campaign Attendees with Let's Calendar

Retrieves campaign attendees from Let's Calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `campaign/:campaignId/attendees`
- **Base URL:** `https://panel.letscalendar.com/api/lc`
- **Official documentation:** [List Campaign Attendees](https://panel.letscalendar.com/docs#apis-GETapi-lc-campaign--campaign_id--attendees)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | The unique identifier of the campaign to get attendees from. |
| `status` | query | `string` | no | Filter by attendee status: N, S, F, U, P, or C. |
| `source` | query | `string` | no | Filter by attendee source such as zapier, api, import, manual, copy, zoom, Public URL, or test-invite. |
| `registered_from` | query | `string` | no | Filter attendees registered from this date in Y-m-d format. |
| `registered_to` | query | `string` | no | Filter attendees registered to this date in Y-m-d format. |
