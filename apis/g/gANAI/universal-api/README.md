# <img src="https://images.mindcloud.co/apps/icons/65c2acb952299dfc9a402183-gan_1781896140381.png" alt="GAN.AI logo" width="28" height="28"> GAN.AI: Universal API

Create AI avatars, speech, and personalized videos with GAN.AI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gANAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gan.ai
- **Vendor API docs:** https://developer.gan.ai/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Voices](actions/list-voices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Avatar

| Action | Method | Description |
| --- | --- | --- |
| [Create Avatar](actions/create-avatar.md) | POST | Creates an avatar in GAN.AI. |
| [Delete Avatars](actions/delete-avatars.md) | DELETE | Deletes avatars in bulk from GAN.AI. |
| [Get Avatar Details](actions/get-avatar-details.md) | GET | Retrieves details for an avatar in GAN.AI. |
| [List Avatars](actions/list-avatars.md) | GET | Retrieves avatars from your GAN.AI account. |

### Avatarinference

| Action | Method | Description |
| --- | --- | --- |
| [Create Avatar Video](actions/create-avatar-video.md) | POST | Creates an avatar video in GAN.AI. |
| [Delete Avatar Videos Bulk](actions/delete-avatar-videos-bulk.md) | DELETE | Deletes avatar videos in bulk from GAN.AI. |
| [Get Avatar Video Details](actions/get-avatar-video-details.md) | GET | Retrieves details for an avatar video in GAN.AI. |
| [List Avatar Videos](actions/list-avatar-videos.md) | GET | Retrieves avatar videos from your GAN.AI account. |

### Consent

| Action | Method | Description |
| --- | --- | --- |
| [Get Consent Passcode](actions/get-consent-passcode.md) | GET | Retrieves a passcode for a GAN.AI consent video. |
| [Submit Consent](actions/submit-consent.md) | POST | Submits a consent video to GAN.AI. |

### Lipsync

| Action | Method | Description |
| --- | --- | --- |
| [Create LipSync](actions/create-lip-sync.md) | POST | Creates a lip-sync video in GAN.AI. |
| [Delete LipSync Videos Bulk](actions/delete-lip-sync-videos-bulk.md) | DELETE | Deletes lip-sync videos in bulk from GAN.AI. |
| [Get LipSync Inference Details](actions/get-lip-sync-inference-details.md) | GET | Retrieves details for a lip-sync inference in GAN.AI. |
| [List User LipSyncs](actions/list-user-lip-syncs.md) | GET | Retrieves lip-sync videos from your GAN.AI account. |

### Photoavatar

| Action | Method | Description |
| --- | --- | --- |
| [Create Photo Avatar](actions/create-photo-avatar.md) | POST | Creates a photo avatar in GAN.AI. |
| [Get Photo Avatar Details](actions/get-photo-avatar-details.md) | GET | Retrieves details for a photo avatar in GAN.AI. |
| [List Photo Avatars](actions/list-photo-avatars.md) | GET | Retrieves photo avatars from your GAN.AI account. |

### Photoavatarinference

| Action | Method | Description |
| --- | --- | --- |
| [Create Photo Avatar Inference](actions/create-photo-avatar-inference.md) | POST | Creates a talking-head video for a photo avatar in GAN.AI. |
| [Get Photo Avatar Inference Details](actions/get-photo-avatar-inference-details.md) | GET | Retrieves details for a photo avatar inference in GAN.AI. |
| [List Photo Avatar Inferences](actions/list-photo-avatar-inferences.md) | GET | Retrieves photo avatar inferences from your GAN.AI account. |

### Soundeffectaudio

| Action | Method | Description |
| --- | --- | --- |
| [Get Sound Effect Audio](actions/get-sound-effect-audio.md) | GET | Retrieves Base64 audio for a sound effect in GAN.AI. |

### Soundeffectjob

| Action | Method | Description |
| --- | --- | --- |
| [Generate Sound Effect](actions/generate-sound-effect.md) | POST | Creates generated sound effects in GAN.AI. |
| [List Sound Effect History](actions/list-sound-effect-history.md) | GET | Retrieves sound effect generation history from GAN.AI. |

### Texttospeechjob

| Action | Method | Description |
| --- | --- | --- |
| [Generate Speech](actions/generate-speech.md) | POST | Creates text-to-speech audio in GAN.AI. |
| [List Text to Speech History](actions/list-text-to-speech-history.md) | GET | Retrieves text-to-speech generation history from GAN.AI. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [Add Voice](actions/add-voice.md) | POST | Creates a custom voice in GAN.AI. |
| [Delete Voice](actions/delete-voice.md) | DELETE | Deletes an existing voice from GAN.AI. |
| [List Voices](actions/list-voices.md) | GET | Retrieves available voice profiles from GAN.AI. |

