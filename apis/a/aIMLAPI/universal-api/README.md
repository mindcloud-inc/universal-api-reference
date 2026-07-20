# <img src="https://images.mindcloud.co/apps/icons/a-imlapi_1775579993316.png" alt="AI/ML API logo" width="28" height="28"> AI/ML API: Universal API

Generate text, image, audio, and video content with AI models

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aIMLAPI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://aimlapi.com
- **Vendor API docs:** https://docs.aimlapi.com/api-references

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Balance](actions/get-account-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Account Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET | Retrieves the account balance from AI/ML API. |

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Claude 3.5 Haiku Chat Completion](actions/create-claude35-haiku-chat-completion.md) | POST |  |
| [Create Gemini 2.5 Flash Chat Completion](actions/create-gemini25-flash-chat-completion.md) | POST | Creates a Gemini 2.5 Flash chat completion in AI/ML API. |
| [Create GPT-4o Mini Chat Completion](actions/create-gpt4o-mini-chat-completion.md) | POST | Creates a GPT-4o Mini chat completion in AI/ML API. |
| [Create GPT-5.2 Chat Completion](actions/create-gpt52-chat-completion.md) | POST | Creates a GPT-5.2 chat completion in AI/ML API. |

### Embedding

| Action | Method | Description |
| --- | --- | --- |
| [Create Embeddings With Text-Embedding-3-Large](actions/create-embeddings-with-text-embedding3-large.md) | POST | Creates text-embedding-3-large embeddings in AI/ML API. |

### Image Generation

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image With Flux Schnell](actions/generate-image-with-flux-schnell.md) | POST | Generates an image with Flux Schnell in AI/ML API. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models](actions/list-models.md) | GET | Retrieves available model IDs from AI/ML API. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create GPT-4o Mini Transcription Task](actions/create-gpt4o-mini-transcription-task.md) | POST | Creates a GPT-4o Mini transcription task in AI/ML API. |
| [Create GPT-4o Transcription Task](actions/create-gpt4o-transcription-task.md) | POST | Creates a GPT-4o transcription task in AI/ML API. |
| [Create Sora 2 Image To Video Task](actions/create-sora2-image-to-video-task.md) | POST | Creates a Sora 2 image-to-video task in AI/ML API. |
| [Create Sora 2 Text To Video Task](actions/create-sora2-text-to-video-task.md) | POST | Creates a Sora 2 text-to-video task in AI/ML API. |
| [Create Speech With GPT-4o Mini TTS](actions/create-speech-with-gpt4o-mini-tts.md) | POST | Creates speech with GPT-4o Mini TTS in AI/ML API. |
| [Create Speech With TTS-1 HD](actions/create-speech-with-tts1-hd.md) | POST | Creates speech with TTS-1 HD in AI/ML API. |
| [Create Wan 2.6 Text To Video Task](actions/create-wan26-text-to-video-task.md) | POST | Creates a Wan 2.6 text-to-video task in AI/ML API. |
| [Edit Image With Flux Dev Image To Image](actions/edit-image-with-flux-dev-image-to-image.md) | POST | Creates an edited image with Flux Dev in AI/ML API. |
| [Edit Image With Flux Kontext Max Image To Image](actions/edit-image-with-flux-kontext-max-image-to-image.md) | POST | Creates an edited image with Flux Kontext Max in AI/ML API. |
| [Edit Image With GPT Image 1](actions/edit-image-with-gpt-image1.md) | POST | Creates an edited image with GPT Image 1 in AI/ML API. |
| [Edit Image With Qwen Image Edit](actions/edit-image-with-qwen-image-edit.md) | POST | Creates an edited image with Qwen Image Edit in AI/ML API. |
| [Generate Image With Gemini 2.5 Flash Image](actions/generate-image-with-gemini25-flash-image.md) | POST | Generates an image with Gemini 2.5 Flash Image in AI/ML API. |
| [Submit Video-01 Generation](actions/submit-video01-generation.md) | POST | Submits a Video-01 generation task in AI/ML API. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Create GPT-4o Response](actions/create-gpt4o-response.md) | POST | Creates a GPT-4o response in AI/ML API. |
| [Create GPT-5 Mini Response](actions/create-gpt5-mini-response.md) | POST | Creates a GPT-5 Mini response in AI/ML API. |
| [Create GPT-5.2 Pro Response](actions/create-gpt52-pro-response.md) | POST | Creates a GPT-5.2 Pro response in AI/ML API. |
| [Create O3 Pro Response](actions/create-o3-pro-response.md) | POST | Creates an O3 Pro response in AI/ML API. |

