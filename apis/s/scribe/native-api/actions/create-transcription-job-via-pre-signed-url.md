# Create Transcription Job Via Pre-Signed URL with 3Scribe

Creates a new transcription job in 3Scribe from a pre-signed upload URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/transcribe`
- **Base URL:** `https://api.3scri.be`
- **Official documentation:** [Create Transcription Job Via Pre-Signed URL](https://helpcentre.3scri.be/developers/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | A descriptive title for the transcription job. |
| `requesturl` | body | `string` | yes | Docs describe this as the filename used when requesting a pre-signed upload URL. |
| `language` | body | `string` | no | ISO language-country code for transcription, such as en-US. |
| `detectlanguage` | body | `boolean` | no | When true, 3Scribe detects the spoken language from the audio. |
