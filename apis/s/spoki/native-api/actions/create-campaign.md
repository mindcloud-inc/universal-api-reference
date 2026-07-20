# Create Campaign with Spoki

Creates a campaign from an existing automation or template.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/`
- **Base URL:** `https://api.spoki.com/api/1`
- **Official documentation:** [Create Campaign](https://documenter.getpostman.com/view/21611004/UzBqnPvF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The campaign name. |
| `scheduled_datetime` | body | `date` | yes | The scheduled send datetime in ISO-8601 format. |
| `status` | body | `string` | yes | The campaign status. |
| `automation` | body | `number` | no | An existing automation ID. |
| `lists[]` | body | `array<number>` | yes | List IDs included in the campaign. |
| `template` | body | `number` | no | An approved template ID. |
