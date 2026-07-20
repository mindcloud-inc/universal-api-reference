# Create Scheduled Screenshot with PagePixels

## Endpoint

- **Method:** `POST`
- **Path:** `/screenshot_configs`
- **Base URL:** `https://api.pagepixels.com`
- **Official documentation:** [Create Scheduled Screenshot](https://pagepixels.com/app/screenshots-api-documentation#scheduled-screenshots-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The public web page URL to schedule for screenshots. |
| `scheduled_every` | query | `number` | yes | How often to capture the screenshot. |
| `scheduled_interval` | query | `string` | yes | The scheduler interval unit such as minutes. |
| `multi_step_actions` | query | `string` | no | JSON array of PagePixels multi-step actions, including change notification rules. |
