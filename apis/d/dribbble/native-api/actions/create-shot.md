# Create Shot with Dribbble

## Endpoint

- **Method:** `POST`
- **Path:** `/shots`
- **Base URL:** `https://api.dribbble.com/v2`
- **Official documentation:** [Create Shot](https://developer.dribbble.com/v2/shots/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | The shot image file. |
| `title` | body | `string` | yes | — |
| `description` | body | `string` | no | — |
| `low_profile` | body | `boolean` | no | — |
| `rebound_source_id` | body | `number` | no | — |
| `scheduled_for` | body | `date` | no | — |
| `tags[]` | body | `array<string>` | no | — |
| `team_id` | body | `number` | no | — |
