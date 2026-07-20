# Create Tool with Hume AI

Creates a new EVI tool in Hume AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/evi/tools`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Create Tool](https://dev.hume.ai/reference/speech-to-speech-evi/tools/create-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Tool name. |
| `parameters` | body | `string` | yes | Stringified JSON schema for the tool parameters. |
