# Video Remove Background with PiAPI/Toolkit

Creates a video background-removal task in PiAPI/Toolkit.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Video Remove Background](https://piapi.ai/docs/tools/video-remove-background-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.video` | body | `string` | yes | Doc-backed PiAPI field for Video Remove Background. |
| `input.invert_output` | body | `boolean` | no | Doc-backed PiAPI field for Video Remove Background. |
