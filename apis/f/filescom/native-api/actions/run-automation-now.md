# Run Automation Now with Files.com

Manually runs an automation in Files.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/automations/:id/manual_run`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [Run Automation Now](https://developers.files.com/rest/resources/automations/automations#manually-run-automation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric automation ID to run. |
