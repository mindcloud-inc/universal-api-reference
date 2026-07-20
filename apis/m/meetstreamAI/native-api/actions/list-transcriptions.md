# List Transcriptions with Meetstream AI

Retrieves bot transcriptions from Meetstream AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/bots/:bot_id/transcriptions`
- **Base URL:** `https://api.meetstream.ai/api/v1`
- **Official documentation:** [List Transcriptions](https://docs.meetstream.ai/api-reference/ap-is/transcription/get-bot-transcriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | path | `string` | yes | The bot identifier. |
