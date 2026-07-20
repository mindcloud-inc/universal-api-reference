# Export Campaign Contacts with Let's Calendar

Exports campaign contacts from Let's Calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `campaign/:campaignId/export-contacts`
- **Base URL:** `https://panel.letscalendar.com/api/lc`
- **Official documentation:** [Export Campaign Contacts](https://panel.letscalendar.com/docs#apis-GETapi-lc-campaign--campaign_id--export-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | path | `string` | yes | The unique identifier of the campaign to export contacts from. |
