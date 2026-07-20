# Save Slack View with Leadberry

## Endpoint

- **Method:** `POST`
- **Path:** `/data/saveSlackView`
- **Base URL:** `https://app.leadberry.com`
- **Official documentation:** [Save Slack View](https://www.leadberry.com/slack)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aid` | body | `string` | no | Leadberry account ID for the selected website view. |
| `id` | body | `string` | no | Leadberry Slack connection ID. |
| `pid` | body | `string` | no | Leadberry profile ID for the selected website view. |
| `wid` | body | `string` | no | Leadberry website ID for the selected website view. |
