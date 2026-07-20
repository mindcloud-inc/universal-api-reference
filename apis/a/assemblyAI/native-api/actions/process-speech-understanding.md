# Process Speech Understanding with AssemblyAI

Creates speech understanding output from an AssemblyAI transcript.

## Endpoint

- **Method:** `POST`
- **Path:** `https://llm-gateway.assemblyai.com/v1/understanding`
- **Base URL:** `https://api.assemblyai.com`
- **Official documentation:** [Process Speech Understanding](https://www.assemblyai.com/docs/api-reference/llm-gateway/create-speech-understanding)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transcript_id` | body | `string` | yes | The ID of the transcript to process. |
| `speech_understanding` | body | `object` | yes | Speech understanding task object with translation, speaker identification, and/or custom formatting request details. |
