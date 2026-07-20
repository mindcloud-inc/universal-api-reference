# Fetch Video Result with ModelsLab

Retrieves a generated video result from ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/video/fetch/{request_id}`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Fetch Video Result](https://docs.modelslab.com/video-api/fetch-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | no | Video generation request ID returned by a generation action. |
