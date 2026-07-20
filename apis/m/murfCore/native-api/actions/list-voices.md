# List Voices with Murf Core

Retrieves available voices from Murf Core.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/speech/voices`
- **Base URL:** `https://api.murf.ai`
- **Official documentation:** [List Voices](https://murf.ai/api/docs/api-reference/voices/get-voices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | query | `string` | no | Optional Murf voice model filter. Valid values are FALCON or GEN2. |
