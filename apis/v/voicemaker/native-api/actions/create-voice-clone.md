# Create Voice Clone with Voicemaker

Creates a new voice clone in Voicemaker.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/voice-clones/add`
- **Base URL:** `https://developer.voicemaker.in`
- **Official documentation:** [Create Voice Clone](https://developer.voicemaker.in/apidocs/create-voice-clone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Display name for the new voice clone. |
| `files` | body | `file` | yes | One or more MP3, WAV, or MP4 audio samples for the clone. Send multiple values as a array. |
| `description` | body | `string` | no | Optional description for the voice clone. |
| `removeBackground` | body | `boolean` | no | Whether to remove background noise from the uploaded samples. |
| `labels` | body | `object` | no | JSON labels object such as category, accent, gender, and age. |
