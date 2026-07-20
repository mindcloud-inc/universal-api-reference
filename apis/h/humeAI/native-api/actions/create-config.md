# Create Config with Hume AI

Creates a new EVI config in Hume AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/evi/configs`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Create Config](https://dev.hume.ai/reference/speech-to-speech-evi/configs/create-config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `evi_version` | body | `string` | yes | EVI version to use. |
| `name` | body | `string` | yes | Config name. |
| `voice.provider` | body | `string` | yes | Voice provider for the config voice. |
| `voice.name` | body | `string` | yes | Voice name for the config voice. |
