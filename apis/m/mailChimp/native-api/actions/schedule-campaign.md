# Schedule Campaign with Mailchimp

Schedules a campaign in Mailchimp.

## Endpoint

- **Method:** `POST`
- **Path:** `campaigns/:campaign_id/actions/schedule`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Schedule Campaign](https://us22.api.mailchimp.com/schema/3.0/Paths/Campaigns/Actions/Schedule.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_delivery` | body | `object` | no | — |
| `campaign_id` | path | `string` | yes | The unique ID for the campaign. |
| `schedule_time` | body | `date` | yes | Scheduled send time. |
| `timewarp` | body | `boolean` | no | Whether to use Timewarp scheduling. |
