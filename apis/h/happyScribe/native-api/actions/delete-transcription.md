# Delete Transcription with HappyScribe

Deletes a transcription from HappyScribe.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/transcriptions/:id`
- **Base URL:** `https://www.happyscribe.com/api/v1`
- **Official documentation:** [Delete Transcription](https://dev.happyscribe.com/sections/product/#transcriptions-delete-a-transcription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The transcription identifier. |
| `permanent` | query | `boolean` | no | Set true for irreversible deletion; otherwise the transcription moves to Trash. |
