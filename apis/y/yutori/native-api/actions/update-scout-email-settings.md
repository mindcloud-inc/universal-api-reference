# Update Scout Email Settings with Yutori

Updates email settings and subscribers for a scout in Yutori.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/scouting/tasks/:scout_id/email-settings`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Update Scout Email Settings](https://docs.yutori.com/reference/scouts-email-settings-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scout_id` | path | `string` | yes | The scout UUID. |
| `skip_email` | body | `boolean` | no | — |
| `subscribers_to_add[]` | body | `array<string>` | no | — |
| `subscribers_to_remove[]` | body | `array<string>` | no | — |
