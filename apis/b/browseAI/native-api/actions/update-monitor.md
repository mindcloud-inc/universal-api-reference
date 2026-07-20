# Update Monitor with Browse AI

Updates an existing monitor in Browse AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/robots/:robotId/monitors/:monitorId`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [Update Monitor](https://developers.browse.ai/v2#tag/monitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `monitorId` | path | `string` | yes | Unique monitor ID  You can find a monitor's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `name` | body | `string` | no | Monitor name |
| `status` | body | `list` | no | If set to `paused`, the monitor will stop working until an `active` status is sent. Accepted values: `active`, `paused`. |
| `inputParameters` | body | `object` | no | An object of input parameters to override default input parameters. |
| `schedules[]` | body | `array<object>` | no | Array of schedules. |
| `schedules[]` | body | `array<object>` | no | Array of schedules. |
| `schedule` | body | `string` | no | recurring schedule. |
| `notifyOnCapturedScreenshotChange` | body | `boolean` | no | If set to `true`, an email notification will be sent to you when a change is detected in captured screenshots. |
| `notifyOnCapturedTextChange` | body | `boolean` | no | If set to `true`, an email notification will be sent to you when a change is detected in captured texts. |
| `capturedScreenshotNotificationThreshold` | body | `number` | no | The "screenshot changed" email notification will be sent to you if the change is greater than this threshold (in percent). |
