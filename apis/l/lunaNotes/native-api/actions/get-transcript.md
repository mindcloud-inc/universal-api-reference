# Get Transcript with LunaNotes

Retrieves a transcript from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/transcripts/:id`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [Get Transcript](https://lunanotes.io/docs/transcripts/get-v1-transcripts-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The LunaNotes transcript ID. |
| `include` | query | `string` | no | Include related video or summaries in the response |
