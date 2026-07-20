# List Uploaded Voices with ModelsLab

Retrieves uploaded voices from ModelsLab.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/voice/voice_list`
- **Base URL:** `https://modelslab.com/api`
- **Official documentation:** [List Uploaded Voices](https://docs.modelslab.com/voice-cloning/voice-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | no | Voice list type: manual, trained, or voice_cover. |
