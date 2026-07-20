# Get YouTube Transcript by Language with LLMLayer

Retrieves a YouTube transcript by language from LLMLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/youtube_transcript`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Get YouTube Transcript by Language](https://docs.llmlayer.ai/api-reference/endpoint/youtube-transcript)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | YouTube video URL. |
| `language` | body | `string` | yes | Transcript language to request. |
