# <img src="https://images.mindcloud.co/apps/icons/segmind-icon-square_1776091214415.png" alt="Segmind logo" width="28" height="28"> Segmind: Universal API

Segmind provides AI model, workflow, storage, endpoint, and fine-tuning APIs for media generation workloads.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/segmind/latest
- **Actions:** 130
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.segmind.com
- **Vendor API docs:** https://docs.segmind.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download Fine-Tuned Model File](actions/download-fine-tuned-model-file.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/segmind/latest/actions/download-fine-tuned-model-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (130)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Upload Asset](actions/upload-asset.md) | POST |  |

### Bytedance Humo Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Bytedance Humo](actions/run-bytedance-humo.md) | POST |  |

### Chatterbox Tts Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Chatterbox TTS](actions/run-chatterbox-tts.md) | POST |  |

### Chatterbox Turbo Tts Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Chatterbox Turbo TTS](actions/run-chatterbox-turbo-tts.md) | POST |  |

### Claude 4 Sonnet Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Claude 4 Sonnet](actions/run-claude-4-sonnet.md) | POST |  |

### Claude 4.5 Sonnet Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Claude 4.5 Sonnet](actions/run-claude-4-5-sonnet.md) | POST |  |

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get User Credits](actions/get-user-credits.md) | GET |  |

### Dataset Upload

| Action | Method | Description |
| --- | --- | --- |
| [Get Fast Flux Dataset Upload URL](actions/get-fast-flux-dataset-upload-url.md) | GET |  |
| [Get Flux Dataset Upload URL](actions/get-flux-dataset-upload-url.md) | GET |  |
| [Get Flux Kontext Dataset Upload URL](actions/get-flux-kontext-dataset-upload-url.md) | GET |  |
| [Get Flux Pro Dataset Upload URL](actions/get-flux-pro-dataset-upload-url.md) | GET |  |
| [Get Qwen Dataset Upload URL](actions/get-qwen-dataset-upload-url.md) | GET |  |

### Dedicated Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Add Dedicated Endpoint](actions/add-dedicated-endpoint.md) | POST |  |
| [Delete Dedicated Endpoint](actions/delete-dedicated-endpoint.md) | DELETE |  |
| [List Dedicated Endpoints](actions/list-dedicated-endpoints.md) | GET |  |
| [Update Dedicated Endpoint](actions/update-dedicated-endpoint.md) | PUT |  |

### Deepseek Chat Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Deepseek Chat](actions/run-deepseek-chat.md) | POST |  |

### Deepseek Reasoner Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Deepseek Reasoner](actions/run-deepseek-reasoner.md) | POST |  |

### Fine-tune Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Fast Flux Fine-Tune Request](actions/create-fast-flux-fine-tune-request.md) | POST |  |
| [Create Flux Fine-Tune Request](actions/create-flux-fine-tune-request.md) | POST |  |
| [Create Flux Kontext Fine-Tune Request](actions/create-flux-kontext-fine-tune-request.md) | POST |  |
| [Create Flux Pro Fine-Tune Request](actions/create-flux-pro-fine-tune-request.md) | POST |  |
| [Create Qwen Fine-Tune Request](actions/create-qwen-fine-tune-request.md) | POST |  |
| [Get Fine-Tune Request Details](actions/get-fine-tune-request-details.md) | GET |  |
| [List Fine-Tune Requests](actions/list-fine-tune-requests.md) | GET |  |

### Fine-tuned Model

| Action | Method | Description |
| --- | --- | --- |
| [Make Fine-Tuned Model Private](actions/make-fine-tuned-model-private.md) | PUT |  |
| [Make Fine-Tuned Model Public](actions/make-fine-tuned-model-public.md) | PUT |  |

### Fine-tuned Model File

| Action | Method | Description |
| --- | --- | --- |
| [Download Fine-Tuned Model File](actions/download-fine-tuned-model-file.md) | GET |  |

### Flux Canny Dev Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Canny Dev](actions/run-flux-canny-dev.md) | POST |  |

### Flux Canny Pro Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Canny Pro](actions/run-flux-canny-pro.md) | POST |  |

### Flux Controlnet Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Controlnet](actions/run-flux-controlnet.md) | POST |  |

### Flux Depth Dev Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Depth Dev](actions/run-flux-depth-dev.md) | POST |  |

### Flux Depth Pro Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Depth Pro](actions/run-flux-depth-pro.md) | POST |  |

### Flux Fill Dev Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Fill Dev](actions/run-flux-fill-dev.md) | POST |  |

### Flux Fill Pro Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Fill Pro](actions/run-flux-fill-pro.md) | POST |  |

### Flux Image To Image Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Image to Image](actions/run-flux-img2img.md) | POST |  |

### Flux Inpaint Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Inpaint](actions/run-flux-inpaint.md) | POST |  |

### Flux Ipadapter Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux IPAdapter](actions/run-flux-ipadapter.md) | POST |  |

### Flux Kontext Dev Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Kontext Dev](actions/run-flux-kontext-dev.md) | POST |  |

### Flux Pulid Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux PuLID](actions/run-flux-pulid.md) | POST |  |

### Flux Redux Dev Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Redux Dev](actions/run-flux-redux-dev.md) | POST |  |

### Flux Redux Schnell Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Redux Schnell](actions/run-flux-redux-schnell.md) | POST |  |

### Flux Schnell Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Flux Schnell](actions/run-flux-schnell.md) | POST |  |

### Gemini 2 Flash Image Generation Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Gemini 2 Flash Image Generation](actions/run-gemini-2-flash-image-generation.md) | POST |  |

### Gemini 2.5 Flash Tts Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Gemini 2.5 Flash TTS](actions/run-gemini-2-5-flash-tts.md) | POST |  |

### Gemini 2.5 Pro Tts Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Gemini 2.5 Pro TTS](actions/run-gemini-2-5-pro-tts.md) | POST |  |

### Gpt 5 Mini Result

| Action | Method | Description |
| --- | --- | --- |
| [Run GPT 5 Mini](actions/run-gpt-5-mini.md) | POST |  |

### Gpt 5 Nano Result

| Action | Method | Description |
| --- | --- | --- |
| [Run GPT 5 Nano](actions/run-gpt-5-nano.md) | POST |  |

### Gpt 5 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run GPT 5](actions/run-gpt-5.md) | POST |  |

### Gpt Image 1 Edit Mini Result

| Action | Method | Description |
| --- | --- | --- |
| [Run GPT Image 1 Edit Mini](actions/run-gpt-image-1-edit-mini.md) | POST |  |

### Gpt Image 1 Mini Result

| Action | Method | Description |
| --- | --- | --- |
| [Run GPT Image 1 Mini](actions/run-gpt-image-1-mini.md) | POST |  |

### Gpt Image 1.5 Edit Result

| Action | Method | Description |
| --- | --- | --- |
| [Run GPT Image 1.5 Edit](actions/run-gpt-image-1-5-edit.md) | POST |  |

### Gpt Image 1.5 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run GPT Image 1.5](actions/run-gpt-image-1-5.md) | POST |  |

### Grok 2 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Grok 2](actions/run-grok-2.md) | POST |  |

### Grok 2 Vision Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Grok 2 Vision](actions/run-grok-2-vision.md) | POST |  |

### Hailuo 02 Fast Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Hailuo 02 Fast](actions/run-hailuo-02-fast.md) | POST |  |

### Hailuo 2.3 Fast Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Hailuo 2.3 Fast](actions/run-hailuo-2-3-fast.md) | POST |  |

### Hailuo 2.3 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Hailuo 2.3](actions/run-hailuo-2-3.md) | POST |  |

### Hidream L1 Fast Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Hidream L1 Fast](actions/run-hidream-l1-fast.md) | POST |  |

### Ideogram 3 Reframe Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Ideogram 3 Reframe](actions/run-ideogram-3-reframe.md) | POST |  |

### Ideogram 3 Remix Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Ideogram 3 Remix](actions/run-ideogram-3-remix.md) | POST |  |

### Ideogram 3 Replace Background Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Ideogram 3 Replace Background](actions/run-ideogram-3-replace-background.md) | POST |  |

### Ideogram Character Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Ideogram Character](actions/run-ideogram-character.md) | POST |  |

### Ideogram Describe Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Ideogram Describe](actions/run-ideogram-describe.md) | POST |  |

### Ideogram Image To Image Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Ideogram Image to Image](actions/run-ideogram-img-2-img.md) | POST |  |

### Ideogram Text To Image Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Ideogram Text to Image](actions/run-ideogram-txt-2-img.md) | POST |  |

### Image 01 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Image 01](actions/run-image-01.md) | POST |  |

### Imagen 4 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Imagen 4](actions/run-imagen-4.md) | POST |  |

### Kimi K2 Instruct 0905 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Kimi K2 Instruct 0905](actions/run-kimi-k2-instruct-0905.md) | POST |  |

### Kling 2.6 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Kling 2.6](actions/run-kling-2-6.md) | POST |  |

### Kling 2.6 Standard Motion Control Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Kling 2.6 Standard Motion Control](actions/run-kling-2-6-standard-motion-control.md) | POST |  |

### Kling 3 Pro Image To Video Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Kling 3 Pro Image to Video](actions/run-kling-3-pro-image2video.md) | POST |  |

### Kling 3 Pro Text To Video Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Kling 3 Pro Text to Video](actions/run-kling-3-pro-text2video.md) | POST |  |

### Kling 3 Text To Image Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Kling 3 Text to Image](actions/run-kling-3-text2image.md) | POST |  |

### Ltx 2 Fast Result

| Action | Method | Description |
| --- | --- | --- |
| [Run LTX 2 Fast](actions/run-ltx-2-fast.md) | POST |  |

### Ltx 2 Pro Result

| Action | Method | Description |
| --- | --- | --- |
| [Run LTX 2 Pro](actions/run-ltx-2-pro.md) | POST |  |

### Ltx Video Result

| Action | Method | Description |
| --- | --- | --- |
| [Run LTX Video](actions/run-ltx-video.md) | POST |  |

### Luma Ray Image To Video Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Luma Ray Image to Video](actions/run-luma-ray-img-2-video.md) | POST |  |

### Luma Ray Text To Video Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Luma Ray Text to Video](actions/run-luma-ray-txt-2-video.md) | POST |  |

### Minimax Ai Live Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Minimax AI Live](actions/run-minimax-ai-live.md) | POST |  |

### Minimax Ai Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Minimax AI](actions/run-minimax-ai.md) | POST |  |

### Mochi 1 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Mochi 1](actions/run-mochi-1.md) | POST |  |

### Model Inference

| Action | Method | Description |
| --- | --- | --- |
| [Run Fast Flux Schnell](actions/run-fast-flux-schnell.md) | POST |  |
| [Run Flux 1.1 Pro Ultra](actions/run-flux-1-1-pro-ultra.md) | POST |  |
| [Run Flux 2 Flex](actions/run-flux-2-flex.md) | POST |  |
| [Run Flux 2 Klein 4B](actions/run-flux-2-klein-4b.md) | POST |  |
| [Run Flux 2 Klein 9B](actions/run-flux-2-klein-9b.md) | POST |  |
| [Run Flux 2 Max](actions/run-flux-2-max.md) | POST |  |
| [Run Flux 2 Pro](actions/run-flux-2-pro.md) | POST |  |
| [Run Flux Dev](actions/run-flux-dev.md) | POST |  |
| [Run Flux Kontext Max](actions/run-flux-kontext-max.md) | POST |  |
| [Run Flux Kontext Pro](actions/run-flux-kontext-pro.md) | POST |  |
| [Run Flux Pro](actions/run-flux-pro.md) | POST |  |
| [Run GPT Image 1](actions/run-gpt-image-1.md) | POST |  |
| [Run GPT Image 1 Edit](actions/run-gpt-image-1-edit.md) | POST |  |
| [Run Hunyuan Video](actions/run-hunyuan-video.md) | POST |  |
| [Run Ideogram 3](actions/run-ideogram-3.md) | POST |  |
| [Run Kling 2.1](actions/run-kling-2-1.md) | POST |  |
| [Run Kling 2.5 Turbo](actions/run-kling-2-5-turbo.md) | POST |  |
| [Run Kling 2.6 Pro Motion Control](actions/run-kling-2-6-pro-motion-control.md) | POST |  |
| [Run Minimax AI Director](actions/run-minimax-ai-director.md) | POST |  |
| [Run Nano Banana](actions/run-nano-banana.md) | POST |  |
| [Run Nano Banana 2](actions/run-nano-banana-2.md) | POST |  |
| [Run Nano Banana Pro](actions/run-nano-banana-pro.md) | POST |  |
| [Run Qwen Image](actions/run-qwen-image.md) | POST |  |
| [Run Seedance Pro](actions/run-seedance-pro.md) | POST |  |
| [Run Seedream 4](actions/run-seedream-4.md) | POST |  |
| [Run Veo 3](actions/run-veo-3.md) | POST |  |
| [Run Wan 2.2 I2V Fast](actions/run-wan-2-2-i2v-fast.md) | POST |  |

### Multi Image Kontext Max Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Multi Image Kontext Max](actions/run-multi-image-kontext-max.md) | POST |  |

### Multi Image Kontext Pro Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Multi Image Kontext Pro](actions/run-multi-image-kontext-pro.md) | POST |  |

### Myshell Tts Result

| Action | Method | Description |
| --- | --- | --- |
| [Run MyShell TTS](actions/run-myshell-tts.md) | POST |  |

### P Image Edit Result

| Action | Method | Description |
| --- | --- | --- |
| [Run P Image Edit](actions/run-p-image-edit.md) | POST |  |

### P Image Result

| Action | Method | Description |
| --- | --- | --- |
| [Run P Image](actions/run-p-image.md) | POST |  |

### Pixverse 4.5 Effects Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Pixverse 4.5 Effects](actions/run-pixverse-4-5-effects.md) | POST |  |

### Pixverse 4.5 Transition Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Pixverse 4.5 Transition](actions/run-pixverse-4-5-transition.md) | POST |  |

### Pixverse 4.5 Video Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Pixverse 4.5 Video](actions/run-pixverse-4-5-video.md) | POST |  |

### Pixverse 5 Extend Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Pixverse 5 Extend](actions/run-pixverse-5-extend.md) | POST |  |

### Pixverse 5 Transition Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Pixverse 5 Transition](actions/run-pixverse-5-transition.md) | POST |  |

### Pixverse 5 Video Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Pixverse 5 Video](actions/run-pixverse-5-video.md) | POST |  |

### Pixverse Image To Video Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Pixverse Image to Video](actions/run-pixverse-image2video.md) | POST |  |

### Pixverse Text To Video Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Pixverse Text to Video](actions/run-pixverse-text2video.md) | POST |  |

### Pixverse Transition Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Pixverse Transition](actions/run-pixverse-transition.md) | POST |  |

### Pixverse V6 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Pixverse V6](actions/run-pixverse-v6.md) | POST |  |

### Qwen Image Edit Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Qwen Image Edit](actions/run-qwen-image-edit.md) | POST |  |

### Recraft V3 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Recraft V3](actions/run-recraft-v3.md) | POST |  |

### Runway Gen4 Turbo Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Runway Gen4 Turbo](actions/run-runway-gen4-turbo.md) | POST |  |

### Sora 2 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Sora 2](actions/run-sora-2.md) | POST |  |

### Veo 2 Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Veo 2](actions/run-veo-2.md) | POST |  |

### Wan 2.2 T2v Fast Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Wan 2.2 T2V Fast](actions/run-wan-2-2-t2v-fast.md) | POST |  |

