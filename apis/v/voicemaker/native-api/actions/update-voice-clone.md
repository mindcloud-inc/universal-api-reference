# Update Voice Clone with Voicemaker

Updates an existing voice clone in Voicemaker.

## Endpoint

- **Method:** `PUT`
- **Path:** `api/v1/voice-clones/{VoiceId}`
- **Base URL:** `https://developer.voicemaker.in`
- **Official documentation:** [Update Voice Clone](https://developer.voicemaker.in/apidocs/edit-voice-clone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `VoiceId` | path | `string` | yes | Voice clone ID to update. |
| `name` | body | `string` | no | Updated name for the voice clone. |
| `description` | body | `string` | no | Updated description for the voice clone. |
| `labels` | body | `object` | no | Updated labels object for the voice clone. |
