# Fetch Voice Result with ModelsLab

Retrieves a generated voice result from ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/voice/fetch/{request_id}`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [Fetch Voice Result](https://docs.modelslab.com/voice-cloning/fetch-voice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | no | Voice generation request ID returned by a generation action. |
