# Send Test Campaign with Emailchef

Sends a test campaign email in Emailchef.

## Endpoint

- **Method:** `PUT`
- **Path:** `campaigns/:id/sendtest`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Send Test Campaign](https://emailchef.com/integration/#/Campaigns/sendTestCampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Emailchef campaign ID. |
| `instance_in.email` | body | `string` | no | Email to send the test to. |
