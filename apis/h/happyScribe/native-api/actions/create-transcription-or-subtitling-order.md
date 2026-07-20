# Create Transcription or Subtitling Order with HappyScribe

Creates a transcription or subtitling order in HappyScribe.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://www.happyscribe.com/api/v1`
- **Official documentation:** [Create Transcription or Subtitling Order](https://dev.happyscribe.com/sections/product/#orders-create-a-transcription-or-subtitling-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `confirm` | body | `boolean` | no | When true, submit the order immediately if there are no errors. |
| `language` | body | `string` | yes | Language code of the source media. |
| `service` | body | `string` | no | Service type: auto for machine transcription or pro for human transcription. |
| `url` | body | `string` | yes | Publicly accessible media URL to ingest for transcription or subtitling. |
