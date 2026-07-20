# Get Models with Uberduck

Retrieves available TTS models from Uberduck.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/models`
- **Base URL:** `https://api.uberduck.ai`
- **Official documentation:** [Get Models](https://docs.uberduck.ai/api-reference/get-models-v-1-models-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `provider` | query | `string` | no | Optional provider filter such as aws, google, or azure. |
