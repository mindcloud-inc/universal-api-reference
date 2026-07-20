# Update Campaign with Spoki

Updates a campaign by ID, including scheduling, status, or list settings.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaigns/{{id}}/`
- **Base URL:** `https://api.spoki.com/api/1`
- **Official documentation:** [Update Campaign](https://documenter.getpostman.com/view/21611004/UzBqnPvF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The campaign ID. |
| `name` | body | `string` | no | The campaign name. |
| `scheduled_datetime` | body | `date` | no | The scheduled send datetime in ISO-8601 format. |
| `status` | body | `string` | no | The campaign status. |
| `automation` | body | `number` | no | An existing automation ID. |
| `lists[]` | body | `array<number>` | no | List IDs included in the campaign. |
