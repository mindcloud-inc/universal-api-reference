# Get Model with Google AI Studio

Retrieves a Gemini model from Google AI Studio.

## Endpoint

- **Method:** `GET`
- **Path:** `v1beta/models/:model`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Get Model](https://ai.google.dev/api/models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | path | `string` | yes | Required. Use the bare model ID (no `models/` prefix), for example `gemini-2.5-pro`. |
