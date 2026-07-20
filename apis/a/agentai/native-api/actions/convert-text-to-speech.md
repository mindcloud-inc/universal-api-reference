# Convert Text To Speech with Agent.ai

Creates a speech audio file from text in Agent.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/output_audio`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Convert Text To Speech](https://docs.agent.ai/api-reference/use-ai/convert-text-to-speech)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text_to_speech` | body | `string` | yes | Text to convert to speech. |
