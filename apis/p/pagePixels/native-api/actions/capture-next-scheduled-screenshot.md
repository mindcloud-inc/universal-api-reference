# Capture Next Scheduled Screenshot with PagePixels

## Endpoint

- **Method:** `POST`
- **Path:** `/screenshot_configs/:screenshot_configuration_id/capture`
- **Base URL:** `https://api.pagepixels.com`
- **Official documentation:** [Capture Next Scheduled Screenshot](https://pagepixels.com/app/screenshots-api-documentation#scheduled-screenshots-capture)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `screenshot_configuration_id` | path | `string` | yes | The screenshot configuration ID to capture immediately. |
