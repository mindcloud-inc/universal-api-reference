# Minimax: Native API Reference

A consolidated summary of Minimax's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://platform.minimax.io/docs/api-reference/api-overview
- **API base URL:** `https://api.minimax.io`

## Authentication

### API Key

Connect with your MiniMax API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://platform.minimax.io/docs/api-reference/file-management-list)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compatible Anthropic Messages](actions/compatible-anthropic-messages.md) | `POST /v1/text/chatcompletion_v2` | [docs](https://platform.minimax.io/docs/api-reference/text-anthropic-api) |
| [Compatible OpenAI Chat Completions](actions/compatible-openai-chat-completions.md) | `POST /v1/text/chatcompletion_v2` | [docs](https://platform.minimax.io/docs/api-reference/text-openai-api) |
| [Create First & Last Frame Video Generation Task](actions/create-first-and-last-frame-video-generation-task.md) | `POST /v1/video_generation` | [docs](https://platform.minimax.io/docs/api-reference/video-generation-fl2v) |
| [Create Speech Generation Task](actions/create-speech-generation-task.md) | `POST /v1/t2a_async_v2` | [docs](https://platform.minimax.io/docs/api-reference/speech-t2a-async-create) |
| [Create Text-to-Video Generation Task](actions/create-text-to-video-generation-task.md) | `POST /v1/video_generation` | [docs](https://platform.minimax.io/docs/api-reference/video-generation-t2v) |
| [Create Video Agent Task](actions/create-video-agent-task.md) | `POST /v1/video_template_generation` | [docs](https://platform.minimax.io/docs/api-reference/video-agent-create) |
| [Delete File](actions/delete-file.md) | `POST /v1/files/delete` | [docs](https://platform.minimax.io/docs/api-reference/file-management-delete) |
| [Delete Voice](actions/delete-voice.md) | `POST /v1/delete_voice` | [docs](https://platform.minimax.io/docs/api-reference/voice-management-delete) |
| [Get Voice](actions/get-voice.md) | `POST /v1/get_voice` | [docs](https://platform.minimax.io/docs/api-reference/voice-management-get) |
| [Image-to-Image Generation](actions/image-to-image-generation.md) | `POST /v1/image_generation` | [docs](https://platform.minimax.io/docs/api-reference/image-generation-i2i) |
| [Image-to-Video Task](actions/image-to-video-task.md) | `POST /v1/video_generation` | [docs](https://platform.minimax.io/docs/api-reference/video-generation-i2v) |
| [List Files](actions/list-files.md) | `GET /v1/files/list` | [docs](https://platform.minimax.io/docs/api-reference/file-management-list) |
| [Lyrics Generation](actions/lyrics-generation.md) | `POST /v1/lyrics_generation` | [docs](https://platform.minimax.io/docs/api-reference/lyrics-generation) |
| [Music Generation](actions/music-generation.md) | `POST /v1/music_generation` | [docs](https://platform.minimax.io/docs/api-reference/music-generation) |
| [Query Speech Generation Task Status](actions/query-speech-generation-task-status.md) | `GET /v1/query/t2a_async_query_v2` | [docs](https://platform.minimax.io/docs/api-reference/speech-t2a-async-query) |
| [Query Video Generation Task Status](actions/query-video-generation-task-status.md) | `GET /v1/query/video_generation` | [docs](https://platform.minimax.io/docs/api-reference/video-generation-query) |
| [Query Video Template Generation Task](actions/query-video-template-generation-task.md) | `GET /v1/query/video_template_generation` | [docs](https://platform.minimax.io/docs/api-reference/video-agent-query) |
| [Retrieve Content](actions/retrieve-content.md) | `GET /v1/files/retrieve_content` | [docs](https://platform.minimax.io/docs/api-reference/file-management-retrieve-content) |
| [Retrieve File](actions/retrieve-file.md) | `GET /v1/files/retrieve` | [docs](https://platform.minimax.io/docs/api-reference/file-management-retrieve) |
| [Subject-Reference to Video Generation Task](actions/subject-reference-to-video-generation-task.md) | `POST /v1/video_generation` | [docs](https://platform.minimax.io/docs/api-reference/video-generation-s2v) |
| [Text Chat](actions/text-chat.md) | `POST /v1/text/chatcompletion_v2` | [docs](https://platform.minimax.io/docs/api-reference/text-chat) |
| [Text Generation](actions/text-generation.md) | `POST /v1/text/chatcompletion_v2` | [docs](https://platform.minimax.io/docs/api-reference/text-post) |
| [Text to Image Generation](actions/text-to-image-generation.md) | `POST /v1/image_generation` | [docs](https://platform.minimax.io/docs/api-reference/image-generation-t2i) |
| [Text to Speech (T2A) HTTP](actions/text-to-speech-t2a-http.md) | `POST /v1/t2a_v2` | [docs](https://platform.minimax.io/docs/api-reference/speech-t2a-http) |
| [Upload Audio for Voice Cloning](actions/upload-audio-for-voice-cloning.md) | `POST /v1/files/upload` | [docs](https://platform.minimax.io/docs/api-reference/voice-cloning-uploadcloneaudio) |
| [Upload File](actions/upload-file.md) | `POST /v1/files/upload` | [docs](https://platform.minimax.io/docs/api-reference/file-management-upload) |
| [Upload Prompt Audio](actions/upload-prompt-audio.md) | `POST /v1/files/upload` | [docs](https://platform.minimax.io/docs/api-reference/voice-cloning-uploadprompt) |
| [Video Download](actions/video-download.md) | `GET /v1/files/retrieve` | [docs](https://platform.minimax.io/docs/api-reference/video-generation-download) |
| [Voice Clone](actions/voice-clone.md) | `POST /v1/voice_clone` | [docs](https://platform.minimax.io/docs/api-reference/voice-cloning-clone) |
| [Voice Design](actions/voice-design.md) | `POST /v1/voice_design` | [docs](https://platform.minimax.io/docs/api-reference/voice-design-design) |
