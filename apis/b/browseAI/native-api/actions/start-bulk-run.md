# Start Bulk Run with Browse AI

Starts a bulk run in Browse AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/robots/:robotId/bulk-runs`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [Start Bulk Run](https://developers.browse.ai/v2#tag/bulk-runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `title` | body | `string` | no | A string that describes the bulk run. |
| `inputParameters[]` | body | `array<object>` | yes | An array of input parameters to override the task's default input parameters. |
| `inputParameters[]` | body | `array<object>` | yes | An array of input parameters to override the task's default input parameters. |
