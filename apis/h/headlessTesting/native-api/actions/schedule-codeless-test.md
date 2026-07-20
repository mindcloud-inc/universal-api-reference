# Schedule Codeless Test with Headless Testing

Schedules a codeless test in Headless Testing.

## Endpoint

- **Method:** `POST`
- **Path:** `/lab/:id/schedule`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Schedule Codeless Test](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The codeless test identifier. |
| `type` | body | `string` | yes | Schedule type: once, daily, weekly, or custom. |
