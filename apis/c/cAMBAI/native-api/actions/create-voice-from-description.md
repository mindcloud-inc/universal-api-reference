# Create Voice from Description with CAMB.AI

Creates a new voice from a description in CAMB.AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/text-to-voice`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Create Voice from Description](https://docs.camb.ai/api-reference/endpoint/create-text-to-voice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Sample text the generated voice should speak. |
| `voice_description` | body | `string` | yes | Detailed description of the desired voice characteristics. |
