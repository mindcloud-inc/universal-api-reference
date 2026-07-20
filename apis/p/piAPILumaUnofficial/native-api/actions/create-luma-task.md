# Create Luma Task with PiAPI/Luma (unofficial)

Creates a new Luma task in PiAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Luma Task](https://piapi.ai/docs/dream-machine/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes | Prompt describing the video to generate. |
| `input.duration` | body | `number` | no | Output video duration in seconds. |
| `input.aspect_ratio` | body | `string` | no | Output aspect ratio for the generated video. |
| `input.start_image` | body | `string` | no | Optional starting image URL for image-to-video generation. |
| `input.end_image` | body | `string` | no | Optional ending image URL for keyframe-guided generation. |
| `input.loop` | body | `boolean` | no | Whether the generated clip should loop. |
