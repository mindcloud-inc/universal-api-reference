# Run Robot Task with Browse AI

Runs a robot task in Browse AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/robots/:robotId/tasks`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [Run Robot Task](https://developers.browse.ai/v2#tag/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `recordVideo` | body | `boolean` | no | Try to record a video while running the task. This is not guaranteed to work as the robot might skip video recording if the site is too heavy. |
| `inputParameters` | body | `object` | no | An object of input parameters to override default input parameters. |
