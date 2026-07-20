# Update Shot with Dribbble

## Endpoint

- **Method:** `PUT`
- **Path:** `/shots/:id`
- **Base URL:** `https://api.dribbble.com/v2`
- **Official documentation:** [Update Shot](https://developer.dribbble.com/v2/shots/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Dribbble shot ID. |
| `title` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `low_profile` | body | `boolean` | no | — |
| `scheduled_for` | body | `date` | no | — |
| `tags[]` | body | `array<string>` | no | — |
| `team_id` | body | `number` | no | — |
