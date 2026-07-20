# Update Codeless Test Report with Headless Testing

Updates a codeless test report in Headless Testing.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lab/:id/report`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Update Codeless Test Report](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cron` | body | `string` | yes | Cron schedule for the report. |
| `email` | body | `string` | yes | The report recipient email address. |
| `id` | path | `string` | yes | The codeless test identifier. |
