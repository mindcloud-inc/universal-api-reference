# Convert Text To Speech with PDF-app

Creates speech audio from text in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/text_to_voice`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Convert Text To Speech](https://pdf-app.net/apidocumentation?type=text_to_voice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrl` | body | `string` | no | Optional text file or HTML file URL to convert to speech. |
| `text` | body | `string` | no | Plain text or SSML content to convert to speech. |
| `voiceId` | body | `string` | no | AWS Polly voice identifier to use for the generated audio. |
| `outputFormat` | body | `string` | no | Audio output format, such as mp3 or ogg_vorbis. |
| `async` | body | `boolean` | no | Whether to run speech generation asynchronously. |
| `type` | body | `string` | no | Speech engine type: longform, generative, neural, or standard. |
| `language` | body | `string` | no | Language code for the selected voice. |
