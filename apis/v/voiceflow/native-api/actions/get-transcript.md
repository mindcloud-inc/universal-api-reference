# Get Transcript with Voiceflow

Retrieves a transcript and its results from Voiceflow.

## Endpoint

- **Method:** `GET`
- **Path:** `https://analytics-api.voiceflow.com/v1/transcript/:transcriptId`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Get Transcript](https://docs.voiceflow.com/api-reference/transcript/get-transcript)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transcriptId` | path | `string` | yes | ID of the transcript to target. |
| `unredacted` | query | `boolean` | no | Return un-redacted logs when available. |
| `filterConversation` | query | `boolean` | no | Only include conversation trace types. |
| `customTraceTypes[]` | query | `array<string>` | no | Additional trace types to include when filterConversation is enabled. |
