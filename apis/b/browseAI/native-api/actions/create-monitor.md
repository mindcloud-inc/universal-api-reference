# Create Monitor with Browse AI

Creates a monitor in Browse AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/robots/:robotId/monitors`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [Create Monitor](https://developers.browse.ai/v2#tag/monitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `name` | body | `string` | yes | Monitor name |
| `inputParameters` | body | `object` | yes | An object of input parameters to override default input parameters. |
| `schedules[]` | body | `array<object>` | no | Array of schedules. |
| `schedules[]` | body | `array<object>` | no | Array of schedules. |
| `schedule` | body | `string` | no | recurring schedule. |
| `notifyOnCapturedScreenshotChange` | body | `boolean` | yes | If set to `true`, an email notification will be sent to you when a change is detected in captured screenshots. |
| `notifyOnCapturedTextChange` | body | `boolean` | yes | If set to `true`, an email notification will be sent to you when a change is detected in captured texts. |
| `capturedScreenshotNotificationThreshold` | body | `number` | yes | The "screenshot changed" email notification will be sent to you if the change is greater than this threshold (in percent). |
