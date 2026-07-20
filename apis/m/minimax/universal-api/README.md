# <img src="https://images.mindcloud.co/apps/icons/minimax-color_1776093491954.png" alt="Minimax logo" width="28" height="28"> Minimax: Universal API

Generate and manage MiniMax text, speech, image, video, music, voice, and file workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/minimax/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://platform.minimax.io
- **Vendor API docs:** https://platform.minimax.io/docs/api-reference/api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Files](actions/list-files.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minimax/latest/actions/list-files?connectionId=$CONNECTION_ID&purpose=t2a_async_input" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Minimax. |
| [List Files](actions/list-files.md) | GET | Retrieves files from Minimax. |
| [Retrieve File](actions/retrieve-file.md) | GET | Retrieves a file from Minimax. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Minimax. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Compatible Anthropic Messages](actions/compatible-anthropic-messages.md) | POST |  |
| [Compatible OpenAI Chat Completions](actions/compatible-openai-chat-completions.md) | POST |  |
| [Create First & Last Frame Video Generation Task](actions/create-first-and-last-frame-video-generation-task.md) | POST | Creates a first-and-last-frame video task in Minimax. |
| [Create Speech Generation Task](actions/create-speech-generation-task.md) | POST | Creates a speech generation task in Minimax. |
| [Create Text-to-Video Generation Task](actions/create-text-to-video-generation-task.md) | POST | Creates a text-to-video generation task in Minimax. |
| [Create Video Agent Task](actions/create-video-agent-task.md) | POST | Creates a video agent task in Minimax. |
| [Delete Voice](actions/delete-voice.md) | DELETE | Deletes a voice from Minimax. |
| [Get Voice](actions/get-voice.md) | GET | Retrieves available voices from Minimax. |
| [Image-to-Image Generation](actions/image-to-image-generation.md) | POST | Creates images from image input in Minimax. |
| [Image-to-Video Task](actions/image-to-video-task.md) | POST | Creates an image-to-video task in Minimax. |
| [Lyrics Generation](actions/lyrics-generation.md) | POST | Creates song lyrics in Minimax. |
| [Music Generation](actions/music-generation.md) | POST | Creates music in Minimax. |
| [Query Speech Generation Task Status](actions/query-speech-generation-task-status.md) | GET | Retrieves a speech generation task status from Minimax. |
| [Query Video Generation Task Status](actions/query-video-generation-task-status.md) | GET | Retrieves a video generation task status from Minimax. |
| [Query Video Template Generation Task](actions/query-video-template-generation-task.md) | GET | Retrieves a video agent task status from Minimax. |
| [Retrieve Content](actions/retrieve-content.md) | GET | Retrieves file content from Minimax. |
| [Subject-Reference to Video Generation Task](actions/subject-reference-to-video-generation-task.md) | POST | Creates a subject-reference video task in Minimax. |
| [Text Chat](actions/text-chat.md) | POST | Creates a chat completion in Minimax. |
| [Text Generation](actions/text-generation.md) | POST | Creates text output in Minimax. |
| [Text to Image Generation](actions/text-to-image-generation.md) | POST | Creates images from text in Minimax. |
| [Text to Speech (T2A) HTTP](actions/text-to-speech-t2a-http.md) | POST | Creates speech from text in Minimax. |
| [Upload Audio for Voice Cloning](actions/upload-audio-for-voice-cloning.md) | POST | Uploads voice-cloning audio to Minimax. |
| [Upload Prompt Audio](actions/upload-prompt-audio.md) | POST | Uploads prompt audio to Minimax. |
| [Video Download](actions/video-download.md) | POST | Retrieves a generated video file from Minimax. |
| [Voice Clone](actions/voice-clone.md) | POST | Creates a cloned voice in Minimax. |
| [Voice Design](actions/voice-design.md) | POST | Creates a designed voice in Minimax. |

