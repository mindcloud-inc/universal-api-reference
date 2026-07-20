# AI/ML API: Native API Reference

A consolidated summary of AI/ML API's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.aimlapi.com/api-references
- **API base URL:** `https://api.aimlapi.com`

## Authentication

### API Key

Authenticate with an AIMLAPI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.aimlapi.com/faq/how-can-i-work-with-my-api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Claude 3.5 Haiku Chat Completion](actions/create-claude35-haiku-chat-completion.md) | `POST /v1/chat/completions` |  |
| [Create Embeddings With Text-Embedding-3-Large](actions/create-embeddings-with-text-embedding3-large.md) | `POST /v1/embeddings` | [docs](https://docs.aimlapi.com/api-references/embedding-models/openai/text-embedding-3-large) |
| [Create Gemini 2.5 Flash Chat Completion](actions/create-gemini25-flash-chat-completion.md) | `POST /v1/chat/completions` | [docs](https://docs.aimlapi.com/api-references/text-models-llm/google/gemini-2.5-flash) |
| [Create GPT-4o Mini Chat Completion](actions/create-gpt4o-mini-chat-completion.md) | `POST /v1/chat/completions` | [docs](https://docs.aimlapi.com/api-references/text-models-llm/openai/gpt-4o-mini) |
| [Create GPT-4o Mini Transcription Task](actions/create-gpt4o-mini-transcription-task.md) | `POST /v1/stt/create` | [docs](https://docs.aimlapi.com/api-references/speech-models/speech-to-text/openai/gpt-4o-mini-transcribe) |
| [Create GPT-4o Response](actions/create-gpt4o-response.md) | `POST /v1/responses` | [docs](https://docs.aimlapi.com/api-references/text-models-llm/openai/gpt-4o) |
| [Create GPT-4o Transcription Task](actions/create-gpt4o-transcription-task.md) | `POST /v1/stt/create` | [docs](https://docs.aimlapi.com/api-references/speech-models/speech-to-text/openai/gpt-4o-transcribe) |
| [Create GPT-5 Mini Response](actions/create-gpt5-mini-response.md) | `POST /v1/responses` | [docs](https://docs.aimlapi.com/api-references/text-models-llm/openai/gpt-5-mini) |
| [Create GPT-5.2 Chat Completion](actions/create-gpt52-chat-completion.md) | `POST /v1/chat/completions` | [docs](https://docs.aimlapi.com/api-references/text-models-llm/openai/gpt-5.2) |
| [Create GPT-5.2 Pro Response](actions/create-gpt52-pro-response.md) | `POST /v1/responses` | [docs](https://docs.aimlapi.com/api-references/text-models-llm/openai/gpt-5.2-pro) |
| [Create O3 Pro Response](actions/create-o3-pro-response.md) | `POST /v1/responses` | [docs](https://docs.aimlapi.com/api-references/text-models-llm/openai/o3-pro) |
| [Create Sora 2 Image To Video Task](actions/create-sora2-image-to-video-task.md) | `POST /v2/video/generations` | [docs](https://docs.aimlapi.com/api-references/video-models/openai/sora-2-i2v) |
| [Create Sora 2 Text To Video Task](actions/create-sora2-text-to-video-task.md) | `POST /v2/video/generations` | [docs](https://docs.aimlapi.com/api-references/video-models/openai/sora-2-t2v) |
| [Create Speech With GPT-4o Mini TTS](actions/create-speech-with-gpt4o-mini-tts.md) | `POST /v1/tts` | [docs](https://docs.aimlapi.com/api-references/speech-models/text-to-speech/openai/gpt-4o-mini-tts) |
| [Create Speech With TTS-1 HD](actions/create-speech-with-tts1-hd.md) | `POST /v1/tts` | [docs](https://docs.aimlapi.com/api-references/speech-models/text-to-speech/openai/tts-1-hd) |
| [Create Wan 2.6 Text To Video Task](actions/create-wan26-text-to-video-task.md) | `POST /v2/video/generations` | [docs](https://docs.aimlapi.com/api-references/video-models/alibaba-cloud/wan-2.6-text-to-video) |
| [Edit Image With Flux Dev Image To Image](actions/edit-image-with-flux-dev-image-to-image.md) | `POST /v1/images/generations` | [docs](https://docs.aimlapi.com/api-references/image-models/flux/flux-dev-image-to-image) |
| [Edit Image With Flux Kontext Max Image To Image](actions/edit-image-with-flux-kontext-max-image-to-image.md) | `POST /v1/images/generations` | [docs](https://docs.aimlapi.com/api-references/image-models/flux/flux-kontext-max-image-to-image) |
| [Edit Image With GPT Image 1](actions/edit-image-with-gpt-image1.md) | `POST /v1/images/edits` | [docs](https://docs.aimlapi.com/api-references/image-models/openai/gpt-image-1) |
| [Edit Image With Qwen Image Edit](actions/edit-image-with-qwen-image-edit.md) | `POST /v1/images/generations` | [docs](https://docs.aimlapi.com/api-references/image-models/alibaba-cloud/qwen-image-edit) |
| [Generate Image With Flux Schnell](actions/generate-image-with-flux-schnell.md) | `POST /v1/images/generations` | [docs](https://docs.aimlapi.com/api-references/image-models/flux/flux-schnell) |
| [Generate Image With Gemini 2.5 Flash Image](actions/generate-image-with-gemini25-flash-image.md) | `POST /v1/images/generations` | [docs](https://docs.aimlapi.com/api-references/image-models/google/gemini-2.5-flash-image) |
| [Get Account Balance](actions/get-account-balance.md) | `GET /v1/billing/balance` | [docs](https://docs.aimlapi.com/api-references/service-endpoints/account-balance) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://docs.aimlapi.com/api-references/model-database) |
| [Submit Video-01 Generation](actions/submit-video01-generation.md) | `POST /v2/video/generations` | [docs](https://docs.aimlapi.com/api-references/video-models/minimax/video-01) |
