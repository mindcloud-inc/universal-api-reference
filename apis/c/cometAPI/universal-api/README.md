# <img src="https://images.mindcloud.co/apps/icons/comet-api-icon_1775836572223.png" alt="CometAPI logo" width="28" height="28"> CometAPI: Universal API

OpenAI-compatible unified AI inference API for model discovery, chat completions, embeddings, image generation, speech, transcription, translation, and moderation through CometAPI.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cometAPI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 86
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cometapi.com
- **Vendor API docs:** https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (86)

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates a chat completion in CometAPI. |

### Embedding

| Action | Method | Description |
| --- | --- | --- |
| [Create Embedding](actions/create-embedding.md) | POST | Creates embeddings in CometAPI. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files-restored.md) | GET |  |

### Image Generation

| Action | Method | Description |
| --- | --- | --- |
| [Create Image Generation](actions/create-image-generation.md) | POST | Creates an image in CometAPI. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Count Message Tokens](actions/count-message-tokens.md) | GET |  |
| [Create Message](actions/create-message.md) | POST | Creates a Claude message in CometAPI. |

### Message Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Message Batch](actions/cancel-message-batch.md) | PUT |  |
| [Create Message Batch](actions/create-message-batch.md) | POST |  |
| [Delete Message Batch](actions/delete-message-batch.md) | DELETE |  |
| [Get Message Batch](actions/get-message-batch.md) | GET |  |
| [List Message Batches](actions/list-message-batches.md) | GET |  |

### Message Batch Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Message Batch Results](actions/get-message-batch-results.md) | GET |  |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Delete Model](actions/delete-model.md) | DELETE |  |
| [Generate Content](actions/generate-content.md) | POST | Generates content with Gemini models in CometAPI. |
| [Get Model](actions/get-model.md) | GET |  |
| [List Models](actions/list-models.md) | GET | Retrieves available models from CometAPI. |

### Moderation

| Action | Method | Description |
| --- | --- | --- |
| [Create Moderation](actions/create-moderation.md) | POST | Creates a moderation in CometAPI. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Response](actions/create-response.md) | POST | Creates a model response in CometAPI. |

### Speech

| Action | Method | Description |
| --- | --- | --- |
| [Create Speech](actions/create-speech.md) | POST | Creates speech audio in CometAPI. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Bria Edit Image](actions/bria-edit-image.md) | POST | Creates a Bria image edit in CometAPI. |
| [Bria Generate Image](actions/bria-generate-image.md) | POST | Creates a Bria image in CometAPI. |
| [Bria Generate Vector](actions/bria-generate-vector.md) | POST | Creates Bria vector graphics in CometAPI. |
| [Bria Get Request](actions/bria-get-request.md) | GET | Retrieves a Bria request from CometAPI. |
| [Bytedance Video Create](actions/bytedance-video-create.md) | POST | Creates a ByteDance video task in CometAPI. |
| [Bytedance Video Get](actions/bytedance-video-get.md) | GET | Retrieves a ByteDance video task from CometAPI. |
| [Flux Generate Image](actions/flux-generate-image.md) | POST | Creates a Flux image in CometAPI. |
| [Flux Get Result](actions/flux-get-result.md) | GET | Retrieves a Flux image result from CometAPI. |
| [Kling Add Video Selection](actions/kling-add-video-selection.md) | POST | Adds a Kling video selection in CometAPI. |
| [Kling Advanced Lip Sync](actions/kling-advanced-lip-sync.md) | POST | Creates a Kling advanced lip-sync task in CometAPI. |
| [Kling Avatar Image To Video](actions/kling-avatar-image-to-video.md) | POST | Creates a Kling avatar video in CometAPI. |
| [Kling Clear Video Selection](actions/kling-clear-video-selection.md) | POST | Clears a Kling video selection in CometAPI. |
| [Kling Create Video Edit Task](actions/kling-create-video-edit-task.md) | POST | Creates a Kling multimodal edit task in CometAPI. |
| [Kling Delete Video Selection](actions/kling-delete-video-selection.md) | POST | Deletes a Kling video selection in CometAPI. |
| [Kling Image Expansion](actions/kling-image-expansion.md) | POST | Creates an expanded Kling image in CometAPI. |
| [Kling Image Generation](actions/kling-image-generation.md) | POST | Creates a Kling image in CometAPI. |
| [Kling Image To Video](actions/kling-image-to-video.md) | POST | Creates a Kling image-to-video task in CometAPI. |
| [Kling Individual Query](actions/kling-individual-query.md) | GET | Retrieves a Kling task from CometAPI. |
| [Kling Initialize Video Editing](actions/kling-initialize-video-editing.md) | POST | Initializes Kling video editing in CometAPI. |
| [Kling Multi Image To Image](actions/kling-multi-image-to-image.md) | POST | Creates a Kling image from multiple images in CometAPI. |
| [Kling Multi Image To Video](actions/kling-multi-image-to-video.md) | POST | Creates a Kling multi-image video in CometAPI. |
| [Kling Omni Query](actions/kling-omni-query.md) | GET | Retrieves a Kling Omni video task from CometAPI. |
| [Kling Omni Video](actions/kling-omni-video.md) | POST | Creates a Kling Omni video in CometAPI. |
| [Kling Preview Video Selection](actions/kling-preview-video-selection.md) | GET | Retrieves a Kling video selection preview in CometAPI. |
| [Kling Text To Video](actions/kling-text-to-video.md) | POST | Creates a Kling text-to-video task in CometAPI. |
| [Kling Video Effects](actions/kling-video-effects.md) | POST | Creates a Kling video effects task in CometAPI. |
| [Kling Video Extension](actions/kling-video-extension.md) | POST | Creates a Kling video extension in CometAPI. |
| [Kling Virtual Try On](actions/kling-virtual-try-on.md) | POST | Creates a Kling virtual try-on image in CometAPI. |
| [Midjourney Blend](actions/midjourney-blend.md) | POST | Creates a Midjourney blend task in CometAPI. |
| [Midjourney Describe](actions/midjourney-describe.md) | POST | Creates a Midjourney prompt from an image in CometAPI. |
| [Midjourney Get Task](actions/midjourney-get-task.md) | GET | Retrieves a Midjourney task from CometAPI. |
| [Midjourney Imagine](actions/midjourney-imagine.md) | POST | Creates a Midjourney imagine task in CometAPI. |
| [Midjourney List Tasks](actions/midjourney-list-tasks.md) | GET | Retrieves Midjourney tasks from CometAPI. |
| [Midjourney Modal](actions/midjourney-modal.md) | POST | Creates a Midjourney modal task in CometAPI. |
| [Midjourney Submit Action](actions/midjourney-submit-action.md) | POST | Creates a Midjourney action task in CometAPI. |
| [Midjourney Submit Editor](actions/midjourney-submit-editor.md) | POST | Creates a Midjourney editor task in CometAPI. |
| [Midjourney Submit Video](actions/midjourney-submit-video.md) | POST | Creates a Midjourney video task in CometAPI. |
| [Replicate Create Prediction](actions/replicate-create-prediction.md) | POST | Creates a Replicate prediction in CometAPI. |
| [Replicate Get Prediction](actions/replicate-get-prediction.md) | GET | Retrieves a Replicate prediction from CometAPI. |
| [Runway Act One](actions/runway-act-one.md) | POST | Creates a Runway Act-One transfer in CometAPI. |
| [Runway Character Performance](actions/runway-character-performance.md) | POST | Creates a Runway character performance task in CometAPI. |
| [Runway Feed Get Task](actions/runway-feed-get-task.md) | GET | Retrieves a Runway feed task from CometAPI. |
| [Runway Generate](actions/runway-generate.md) | POST | Creates a Runway text-to-video task in CometAPI. |
| [Runway Generate Image To Video](actions/runway-generate-image-to-video.md) | POST | Creates a Runway image-to-video task in CometAPI. |
| [Runway Get Task](actions/runway-get-task.md) | GET | Retrieves a Runway task from CometAPI. |
| [Runway Image To Video](actions/runway-image-to-video.md) | POST | Creates a Runway image-to-video task in CometAPI. |
| [Runway Video To Video](actions/runway-video-to-video.md) | POST | Creates a Runway video-to-video task in CometAPI. |
| [Runway Video Upscale](actions/runway-video-upscale.md) | POST | Creates a Runway video upscale task in CometAPI. |
| [Runway Video2Video Style Redraw](actions/runway-video2video-style-redraw.md) | POST | Creates a Runway video style transfer in CometAPI. |
| [Sora Create Video](actions/sora-create-video.md) | POST | Creates a Sora video task in CometAPI. |
| [Sora Get Video](actions/sora-get-video.md) | GET | Retrieves a Sora video task from CometAPI. |
| [Sora Get Video Content](actions/sora-get-video-content.md) | GET | Retrieves Sora video content from CometAPI. |
| [Sora Remix Video](actions/sora-remix-video.md) | POST | Creates a Sora video remix in CometAPI. |
| [Veo3 Create Video](actions/veo3-create-video.md) | POST | Creates a Veo 3 video task in CometAPI. |
| [Veo3 Get Video](actions/veo3-get-video.md) | GET | Retrieves a Veo 3 video task from CometAPI. |
| [xAI Get Video Result](actions/xai-get-video-result.md) | GET | Retrieves an xAI video result from CometAPI. |
| [xAI Video Edit](actions/xai-video-edit.md) | POST | Creates an xAI video edit in CometAPI. |
| [xAI Video Generation](actions/xai-video-generation.md) | POST | Creates an xAI video generation task in CometAPI. |

### Transcription

| Action | Method | Description |
| --- | --- | --- |
| [Create Transcription](actions/create-transcription.md) | POST | Creates a transcription in CometAPI. |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [Create Translation](actions/create-translation.md) | POST | Creates an audio translation in CometAPI. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Bytedance Image Edit](actions/bytedance-image-edit.md) | POST | Creates a ByteDance image edit in CometAPI. |
| [Kling Identify Face](actions/kling-identify-face.md) | POST | Identifies faces for Kling lip-sync in CometAPI. |
| [Kling Image Recognize](actions/kling-image-recognize.md) | POST | Recognizes an image with Kling in CometAPI. |
| [Kling Text To Audio](actions/kling-text-to-audio.md) | POST | Creates audio from text with Kling in CometAPI. |
| [Kling TTS](actions/kling-tts.md) | POST | Creates speech audio with Kling in CometAPI. |
| [Kling Video To Audio](actions/kling-video-to-audio.md) | POST | Creates audio from video with Kling in CometAPI. |
| [OpenAI Image Edit](actions/openai-image-edit.md) | POST | Creates an image edit in CometAPI. |

