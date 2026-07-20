# Create Single Use Token with ElevenLabs

Creates a single-use token in ElevenLabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/single-use-token/:token_type`
- **Base URL:** `https://api.elevenlabs.io/v1`
- **Official documentation:** [Create Single Use Token](https://elevenlabs.io/docs/api-reference/tokens/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token_type` | path | `string` | yes | The single-use token type. |
