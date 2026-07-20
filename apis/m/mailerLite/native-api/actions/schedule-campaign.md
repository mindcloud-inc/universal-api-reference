# Schedule Campaign with MailerLite

Schedules a campaign in MailerLite, or sends it immediately.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaignId/schedule`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Schedule Campaign](https://developers.mailerlite.com/docs/campaigns#schedule-a-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Draft or ready campaign ID to schedule. |
| `delivery` | body | `string` | yes | Delivery mode for the campaign. |
| `schedule` | body | `object` | no | Schedule settings object. |
| `schedule.date` | body | `date` | yes | Future delivery date. |
| `schedule.hours` | body | `string` | yes | Delivery hour in HH format. |
| `schedule.minutes` | body | `string` | yes | Delivery minute in ii format. |
| `schedule.timezone_id` | body | `number` | no | Timezone ID for scheduled delivery. |
