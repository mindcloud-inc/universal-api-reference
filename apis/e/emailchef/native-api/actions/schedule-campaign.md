# Schedule Campaign with Emailchef

Schedules a campaign in Emailchef.

## Endpoint

- **Method:** `PUT`
- **Path:** `campaigns/:id/schedule`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Schedule Campaign](https://emailchef.com/integration/#/Campaigns/scheduleCampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Emailchef campaign ID. |
| `instance_in.timezone` | body | `number` | no | Timezone ID. |
| `instance_in.scheduled_time` | body | `date` | no | Scheduled send time. |
