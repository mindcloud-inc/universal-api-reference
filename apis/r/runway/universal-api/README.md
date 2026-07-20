# <img src="https://images.mindcloud.co/apps/icons/images-8_1774442132031.png" alt="Runway logo" width="28" height="28"> Runway: Universal API

Generate videos and characters with Runway AI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/runway/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://runwayml.com/
- **Vendor API docs:** https://docs.dev.runwayml.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization Information](actions/get-organization-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runway/latest/actions/get-organization-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Avatar

| Action | Method | Description |
| --- | --- | --- |
| [Create Avatar](actions/create-avatar.md) | POST | Creates an avatar in Runway. |
| [Delete Avatar](actions/delete-avatar.md) | DELETE | Deletes an avatar from Runway. |
| [Get Avatar](actions/get-avatar.md) | GET | Retrieves an avatar from Runway. |
| [List Avatars](actions/list-avatars.md) | GET | Retrieves avatars from Runway. |
| [Update Avatar](actions/update-avatar.md) | PUT | Updates an avatar in Runway. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a document in Runway. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from Runway. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Runway. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Runway. |
| [Update Document](actions/update-document.md) | PUT | Updates a document in Runway. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Information](actions/get-organization-information.md) | GET | Retrieves organization information from Runway. |

### Organizationusage

| Action | Method | Description |
| --- | --- | --- |
| [Query Credit Usage](actions/query-credit-usage.md) | GET | Retrieves organization credit usage from Runway. |

### Realtimesession

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Realtime Session](actions/cancel-realtime-session.md) | DELETE | Cancels a realtime session in Runway. |
| [Create Realtime Session](actions/create-realtime-session.md) | POST | Creates a realtime session in Runway. |
| [Get Realtime Session](actions/get-realtime-session.md) | GET | Retrieves a realtime session from Runway. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Or Delete Task](actions/cancel-or-delete-task.md) | DELETE | Cancels or deletes a task in Runway. |
| [Control A Character](actions/control-a-character.md) | POST | Creates a character performance task in Runway. |
| [Generate Sound Effects](actions/generate-sound-effects.md) | POST | Creates a sound effect generation task in Runway. |
| [Get Task Detail](actions/get-task-detail.md) | GET | Retrieves task details from Runway. |
| [Image To Video](actions/image-to-video.md) | POST | Creates a video generation task from an image in Runway. |
| [Speech To Speech](actions/speech-to-speech.md) | POST | Creates a speech-to-speech generation task in Runway. |
| [Text Or Image To Image](actions/text-or-image-to-image.md) | POST | Creates an image generation task from text or images in Runway. |
| [Text To Speech](actions/text-to-speech.md) | POST | Creates a text-to-speech generation task in Runway. |
| [Text To Video](actions/text-to-video.md) | POST | Creates a video generation task from text in Runway. |
| [Video To Video](actions/video-to-video.md) | POST | Creates a video generation task from a video in Runway. |
| [Voice Dubbing](actions/voice-dubbing.md) | POST | Creates a voice dubbing task in Runway. |
| [Voice Isolation](actions/voice-isolation.md) | POST | Creates a voice isolation task in Runway. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Creates an ephemeral file upload in Runway. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [Delete Voice](actions/delete-voice.md) | DELETE | Deletes a voice from Runway. |
| [Get Voice](actions/get-voice.md) | GET | Retrieves a voice from Runway. |
| [List Voices](actions/list-voices.md) | GET | Retrieves voices from Runway. |

### Voicepreview

| Action | Method | Description |
| --- | --- | --- |
| [Preview Voice](actions/preview-voice.md) | POST | Creates a voice preview in Runway. |

