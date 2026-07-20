# Segmind: Native API Reference

A consolidated summary of Segmind's API configuration and 130 documented operations, with links to official documentation.

- **Official docs:** https://docs.segmind.com
- **API base URL:** `https://api.segmind.com`

## Authentication

### API Key

Custom header authentication for Segmind APIs using x-api-key.

### Credentials

- **API Key:** `apiKey` · required · Segmind tenant API key.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.segmind.com/api-reference)

## Endpoints (130 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Dedicated Endpoint](actions/add-dedicated-endpoint.md) | `POST https://api.spotstage.segmind.com/endpoint/add` | [docs](https://docs.segmind.com/dedicated-endpoints/endpoint-apis) |
| [Create Fast Flux Fine-Tune Request](actions/create-fast-flux-fine-tune-request.md) | `POST /finetune/request/submit` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/fast-flux-fine-tuning-api) |
| [Create Flux Fine-Tune Request](actions/create-flux-fine-tune-request.md) | `POST /finetune/request/submit` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/flux-fine-tuning-api) |
| [Create Flux Kontext Fine-Tune Request](actions/create-flux-kontext-fine-tune-request.md) | `POST /finetune/request/submit` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/flux-kontext-fine-tuning-api) |
| [Create Flux Pro Fine-Tune Request](actions/create-flux-pro-fine-tune-request.md) | `POST /finetune/request/submit` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/flux-pro-fine-tuning-api) |
| [Create Qwen Fine-Tune Request](actions/create-qwen-fine-tune-request.md) | `POST /finetune/request/submit` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/qwen-fine-tuning-api) |
| [Delete Dedicated Endpoint](actions/delete-dedicated-endpoint.md) | `POST https://api.spotprod.segmind.com/endpoint/delete` | [docs](https://docs.segmind.com/dedicated-endpoints/endpoint-apis) |
| [Download Fine-Tuned Model File](actions/download-fine-tuned-model-file.md) | `GET /finetune/request/file/download` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/flux-fine-tuning-api) |
| [Get Fast Flux Dataset Upload URL](actions/get-fast-flux-dataset-upload-url.md) | `GET /finetune/request/upload/pre-signed-url` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/fast-flux-fine-tuning-api) |
| [Get Fine-Tune Request Details](actions/get-fine-tune-request-details.md) | `GET /finetune/request/details` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/flux-fine-tuning-api) |
| [Get Flux Dataset Upload URL](actions/get-flux-dataset-upload-url.md) | `GET /finetune/request/upload/pre-signed-url` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/flux-fine-tuning-api) |
| [Get Flux Kontext Dataset Upload URL](actions/get-flux-kontext-dataset-upload-url.md) | `GET /finetune/request/upload/pre-signed-url` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/flux-kontext-fine-tuning-api) |
| [Get Flux Pro Dataset Upload URL](actions/get-flux-pro-dataset-upload-url.md) | `GET /finetune/request/upload/pre-signed-url` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/flux-pro-fine-tuning-api) |
| [Get Qwen Dataset Upload URL](actions/get-qwen-dataset-upload-url.md) | `GET /finetune/request/upload/pre-signed-url` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/qwen-fine-tuning-api) |
| [Get User Credits](actions/get-user-credits.md) | `GET /v1/get-user-credits` | [docs](https://docs.segmind.com/api-reference/account-and-billing-apis) |
| [List Dedicated Endpoints](actions/list-dedicated-endpoints.md) | `GET https://api.spotprod.segmind.com/endpoint/list` | [docs](https://docs.segmind.com/dedicated-endpoints/endpoint-apis) |
| [List Fine-Tune Requests](actions/list-fine-tune-requests.md) | `GET /finetune/request/list` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/flux-fine-tuning-api) |
| [Make Fine-Tuned Model Private](actions/make-fine-tuned-model-private.md) | `PUT /finetune/request/access-update` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/flux-fine-tuning-api) |
| [Make Fine-Tuned Model Public](actions/make-fine-tuned-model-public.md) | `PUT /finetune/request/access-update` | [docs](https://docs.segmind.com/readme/flux-fine-tuning/flux-fine-tuning-api) |
| [Run Bytedance Humo](actions/run-bytedance-humo.md) | `POST /v1/bytedance-humo` | [docs](https://www.segmind.com/models/bytedance-humo/api) |
| [Run Chatterbox TTS](actions/run-chatterbox-tts.md) | `POST /v1/chatterbox-tts` | [docs](https://www.segmind.com/models/chatterbox-tts/api) |
| [Run Chatterbox Turbo TTS](actions/run-chatterbox-turbo-tts.md) | `POST /v1/chatterbox-turbo-tts` | [docs](https://www.segmind.com/models/chatterbox-turbo-tts/api) |
| [Run Claude 4.5 Sonnet](actions/run-claude-4-5-sonnet.md) | `POST /v1/claude-4.5-sonnet` | [docs](https://www.segmind.com/models/claude-4.5-sonnet/api) |
| [Run Claude 4 Sonnet](actions/run-claude-4-sonnet.md) | `POST /v1/claude-4-sonnet` | [docs](https://www.segmind.com/models/claude-4-sonnet/api) |
| [Run Deepseek Chat](actions/run-deepseek-chat.md) | `POST /v1/deepseek-chat` | [docs](https://www.segmind.com/models/deepseek-chat/api) |
| [Run Deepseek Reasoner](actions/run-deepseek-reasoner.md) | `POST /v1/deepseek-reasoner` | [docs](https://www.segmind.com/models/deepseek-reasoner/api) |
| [Run Fast Flux Schnell](actions/run-fast-flux-schnell.md) | `POST /v1/fast-flux-schnell` | [docs](https://www.segmind.com/pixelflows/all/flux) |
| [Run Flux 1.1 Pro Ultra](actions/run-flux-1-1-pro-ultra.md) | `POST /v1/flux-1.1-pro-ultra` | [docs](https://www.segmind.com/pixelflows/all/flux) |
| [Run Flux 2 Flex](actions/run-flux-2-flex.md) | `POST /v1/flux-2-flex` | [docs](https://www.segmind.com/models/all/flux) |
| [Run Flux 2 Klein 4B](actions/run-flux-2-klein-4b.md) | `POST /v1/flux-2-klein-4b` | [docs](https://www.segmind.com/models/all/flux) |
| [Run Flux 2 Klein 9B](actions/run-flux-2-klein-9b.md) | `POST /v1/flux-2-klein-9b` | [docs](https://www.segmind.com/models/all/flux) |
| [Run Flux 2 Max](actions/run-flux-2-max.md) | `POST /v1/flux-2-max` | [docs](https://www.segmind.com/models/all/flux) |
| [Run Flux 2 Pro](actions/run-flux-2-pro.md) | `POST /v1/flux-2-pro` | [docs](https://www.segmind.com/models/all/flux) |
| [Run Flux Canny Dev](actions/run-flux-canny-dev.md) | `POST /v1/flux-canny-dev` | [docs](https://www.segmind.com/models/flux-canny-dev/api) |
| [Run Flux Canny Pro](actions/run-flux-canny-pro.md) | `POST /v1/flux-canny-pro` | [docs](https://www.segmind.com/models/flux-canny-pro/api) |
| [Run Flux Controlnet](actions/run-flux-controlnet.md) | `POST /v1/flux-controlnet` | [docs](https://www.segmind.com/models/flux-controlnet/api) |
| [Run Flux Depth Dev](actions/run-flux-depth-dev.md) | `POST /v1/flux-depth-dev` | [docs](https://www.segmind.com/models/flux-depth-dev/api) |
| [Run Flux Depth Pro](actions/run-flux-depth-pro.md) | `POST /v1/flux-depth-pro` | [docs](https://www.segmind.com/models/flux-depth-pro/api) |
| [Run Flux Dev](actions/run-flux-dev.md) | `POST /v1/flux-dev` | [docs](https://www.segmind.com/pixelflows/all/flux) |
| [Run Flux Fill Dev](actions/run-flux-fill-dev.md) | `POST /v1/flux-fill-dev` | [docs](https://www.segmind.com/models/flux-fill-dev/api) |
| [Run Flux Fill Pro](actions/run-flux-fill-pro.md) | `POST /v1/flux-fill-pro` | [docs](https://www.segmind.com/models/flux-fill-pro/api) |
| [Run Flux Image to Image](actions/run-flux-img2img.md) | `POST /v1/flux-img2img` | [docs](https://www.segmind.com/models/flux-img2img/api) |
| [Run Flux Inpaint](actions/run-flux-inpaint.md) | `POST /v1/flux-inpaint` | [docs](https://www.segmind.com/models/flux-inpaint/api) |
| [Run Flux IPAdapter](actions/run-flux-ipadapter.md) | `POST /v1/flux-ipadapter` | [docs](https://www.segmind.com/models/flux-ipadapter/api) |
| [Run Flux Kontext Dev](actions/run-flux-kontext-dev.md) | `POST /v1/flux-kontext-dev` | [docs](https://www.segmind.com/models/flux-kontext-dev/api) |
| [Run Flux Kontext Max](actions/run-flux-kontext-max.md) | `POST /v1/flux-kontext-max` | [docs](https://www.segmind.com/pixelflows/all/flux) |
| [Run Flux Kontext Pro](actions/run-flux-kontext-pro.md) | `POST /v1/flux-kontext-pro` | [docs](https://www.segmind.com/pixelflows/all/flux) |
| [Run Flux Pro](actions/run-flux-pro.md) | `POST /v1/flux-pro` | [docs](https://www.segmind.com/pixelflows/all/flux) |
| [Run Flux PuLID](actions/run-flux-pulid.md) | `POST /v1/flux-pulid` | [docs](https://www.segmind.com/models/flux-pulid/api) |
| [Run Flux Redux Dev](actions/run-flux-redux-dev.md) | `POST /v1/flux-redux-dev` | [docs](https://www.segmind.com/models/flux-redux-dev/api) |
| [Run Flux Redux Schnell](actions/run-flux-redux-schnell.md) | `POST /v1/flux-redux-schnell` | [docs](https://www.segmind.com/models/flux-redux-schnell/api) |
| [Run Flux Schnell](actions/run-flux-schnell.md) | `POST /v1/flux-schnell` | [docs](https://www.segmind.com/models/flux-schnell/api) |
| [Run Gemini 2.5 Flash TTS](actions/run-gemini-2-5-flash-tts.md) | `POST /v1/gemini-2.5-flash-tts` | [docs](https://www.segmind.com/models/gemini-2.5-flash-tts/api) |
| [Run Gemini 2.5 Pro TTS](actions/run-gemini-2-5-pro-tts.md) | `POST /v1/gemini-2.5-pro-tts` | [docs](https://www.segmind.com/models/gemini-2.5-pro-tts/api) |
| [Run Gemini 2 Flash Image Generation](actions/run-gemini-2-flash-image-generation.md) | `POST /v1/gemini-2-flash-image-generation` | [docs](https://www.segmind.com/models/gemini-2-flash-image-generation/api) |
| [Run GPT 5](actions/run-gpt-5.md) | `POST /v1/gpt-5` | [docs](https://www.segmind.com/models/gpt-5/api) |
| [Run GPT 5 Mini](actions/run-gpt-5-mini.md) | `POST /v1/gpt-5-mini` | [docs](https://www.segmind.com/models/gpt-5-mini/api) |
| [Run GPT 5 Nano](actions/run-gpt-5-nano.md) | `POST /v1/gpt-5-nano` | [docs](https://www.segmind.com/models/gpt-5-nano/api) |
| [Run GPT Image 1](actions/run-gpt-image-1.md) | `POST /v1/gpt-image-1` | [docs](https://www.segmind.com/pixelflows/all/gpt-image-1) |
| [Run GPT Image 1.5](actions/run-gpt-image-1-5.md) | `POST /v1/gpt-image-1.5` | [docs](https://www.segmind.com/models/gpt-image-1.5/api) |
| [Run GPT Image 1.5 Edit](actions/run-gpt-image-1-5-edit.md) | `POST /v1/gpt-image-1.5-edit` | [docs](https://www.segmind.com/models/gpt-image-1.5-edit/api) |
| [Run GPT Image 1 Edit](actions/run-gpt-image-1-edit.md) | `POST /v1/gpt-image-1-edit` | [docs](https://www.segmind.com/pixelflows/all/gpt-image-1-edit-workflows) |
| [Run GPT Image 1 Edit Mini](actions/run-gpt-image-1-edit-mini.md) | `POST /v1/gpt-image-1-edit-mini` | [docs](https://www.segmind.com/models/gpt-image-1-edit-mini/api) |
| [Run GPT Image 1 Mini](actions/run-gpt-image-1-mini.md) | `POST /v1/gpt-image-1-mini` | [docs](https://www.segmind.com/models/gpt-image-1-mini/api) |
| [Run Grok 2](actions/run-grok-2.md) | `POST /v1/grok-2` | [docs](https://www.segmind.com/models/grok-2/api) |
| [Run Grok 2 Vision](actions/run-grok-2-vision.md) | `POST /v1/grok-2-vision` | [docs](https://www.segmind.com/models/grok-2-vision/api) |
| [Run Hailuo 02 Fast](actions/run-hailuo-02-fast.md) | `POST /v1/hailuo-02-fast` | [docs](https://www.segmind.com/models/hailuo-02-fast/api) |
| [Run Hailuo 2.3](actions/run-hailuo-2-3.md) | `POST /v1/hailuo-2.3` | [docs](https://www.segmind.com/models/hailuo-2.3/api) |
| [Run Hailuo 2.3 Fast](actions/run-hailuo-2-3-fast.md) | `POST /v1/hailuo-2.3-fast` | [docs](https://www.segmind.com/models/hailuo-2.3-fast/api) |
| [Run Hidream L1 Fast](actions/run-hidream-l1-fast.md) | `POST /v1/hidream-l1-fast` | [docs](https://www.segmind.com/models/hidream-l1-fast/api) |
| [Run Hunyuan Video](actions/run-hunyuan-video.md) | `POST /v1/hunyuan-video` | [docs](https://www.segmind.com/models/all/hunyuan) |
| [Run Ideogram 3](actions/run-ideogram-3.md) | `POST /v1/ideogram-3` | [docs](https://www.segmind.com/pixelflows/all/ideogram-3-workflows) |
| [Run Ideogram 3 Reframe](actions/run-ideogram-3-reframe.md) | `POST /v1/ideogram-3-reframe` | [docs](https://www.segmind.com/models/ideogram-3-reframe/api) |
| [Run Ideogram 3 Remix](actions/run-ideogram-3-remix.md) | `POST /v1/ideogram-3-remix` | [docs](https://www.segmind.com/models/ideogram-3-remix/api) |
| [Run Ideogram 3 Replace Background](actions/run-ideogram-3-replace-background.md) | `POST /v1/ideogram-3-replace-background` | [docs](https://www.segmind.com/models/ideogram-3-replace-background/api) |
| [Run Ideogram Character](actions/run-ideogram-character.md) | `POST /v1/ideogram-character` | [docs](https://www.segmind.com/models/ideogram-character/api) |
| [Run Ideogram Describe](actions/run-ideogram-describe.md) | `POST /v1/ideogram-describe` | [docs](https://www.segmind.com/models/ideogram-describe/api) |
| [Run Ideogram Image to Image](actions/run-ideogram-img-2-img.md) | `POST /v1/ideogram-img-2-img` | [docs](https://www.segmind.com/models/ideogram-img-2-img/api) |
| [Run Ideogram Text to Image](actions/run-ideogram-txt-2-img.md) | `POST /v1/ideogram-txt-2-img` | [docs](https://www.segmind.com/models/ideogram-txt-2-img/api) |
| [Run Image 01](actions/run-image-01.md) | `POST /v1/image-01` | [docs](https://www.segmind.com/models/image-01/api) |
| [Run Imagen 4](actions/run-imagen-4.md) | `POST /v1/imagen-4` | [docs](https://www.segmind.com/models/imagen-4/api) |
| [Run Kimi K2 Instruct 0905](actions/run-kimi-k2-instruct-0905.md) | `POST /v1/kimi-k2-instruct-0905` | [docs](https://www.segmind.com/models/kimi-k2-instruct-0905/api) |
| [Run Kling 2.1](actions/run-kling-2-1.md) | `POST /v1/kling-2.1` | [docs](https://www.segmind.com/pixelflows/all/kling) |
| [Run Kling 2.5 Turbo](actions/run-kling-2-5-turbo.md) | `POST /v1/kling-2.5-turbo` | [docs](https://www.segmind.com/pixelflows/all/kling) |
| [Run Kling 2.6](actions/run-kling-2-6.md) | `POST /v1/kling-2.6` | [docs](https://www.segmind.com/models/kling-2.6/api) |
| [Run Kling 2.6 Pro Motion Control](actions/run-kling-2-6-pro-motion-control.md) | `POST /v1/kling-2.6-pro-motion-control` | [docs](https://www.segmind.com/pixelflows/all/kling-2-6-pro-motion-control-workflows) |
| [Run Kling 2.6 Standard Motion Control](actions/run-kling-2-6-standard-motion-control.md) | `POST /v1/kling-2.6-standard-motion-control` | [docs](https://www.segmind.com/models/kling-2.6-standard-motion-control/api) |
| [Run Kling 3 Pro Image to Video](actions/run-kling-3-pro-image2video.md) | `POST /v1/kling-3-pro-image2video` | [docs](https://www.segmind.com/models/kling-3-pro-image2video/api) |
| [Run Kling 3 Pro Text to Video](actions/run-kling-3-pro-text2video.md) | `POST /v1/kling-3-pro-text2video` | [docs](https://www.segmind.com/models/kling-3-pro-text2video/api) |
| [Run Kling 3 Text to Image](actions/run-kling-3-text2image.md) | `POST /v1/kling-3-text2image` | [docs](https://www.segmind.com/models/kling-3-text2image/api) |
| [Run LTX 2 Fast](actions/run-ltx-2-fast.md) | `POST /v1/ltx-2-fast` | [docs](https://www.segmind.com/models/ltx-2-fast/api) |
| [Run LTX 2 Pro](actions/run-ltx-2-pro.md) | `POST /v1/ltx-2-pro` | [docs](https://www.segmind.com/models/ltx-2-pro/api) |
| [Run LTX Video](actions/run-ltx-video.md) | `POST /v1/ltx-video` | [docs](https://www.segmind.com/models/ltx-video/api) |
| [Run Luma Ray Image to Video](actions/run-luma-ray-img-2-video.md) | `POST /v1/luma-ray-img-2-video` | [docs](https://www.segmind.com/models/luma-ray-img-2-video/api) |
| [Run Luma Ray Text to Video](actions/run-luma-ray-txt-2-video.md) | `POST /v1/luma-ray-txt-2-video` | [docs](https://www.segmind.com/models/luma-ray-txt-2-video/api) |
| [Run Minimax AI](actions/run-minimax-ai.md) | `POST /v1/minimax-ai` | [docs](https://www.segmind.com/models/minimax-ai/api) |
| [Run Minimax AI Director](actions/run-minimax-ai-director.md) | `POST /v1/minimax-ai-director` | [docs](https://www.segmind.com/pixelflows/all/minimax-ai-director-workflows) |
| [Run Minimax AI Live](actions/run-minimax-ai-live.md) | `POST /v1/minimax-ai-live` | [docs](https://www.segmind.com/models/minimax-ai-live/api) |
| [Run Mochi 1](actions/run-mochi-1.md) | `POST /v1/mochi-1` | [docs](https://www.segmind.com/models/mochi-1/api) |
| [Run Multi Image Kontext Max](actions/run-multi-image-kontext-max.md) | `POST /v1/multi-image-kontext-max` | [docs](https://www.segmind.com/models/multi-image-kontext-max/api) |
| [Run Multi Image Kontext Pro](actions/run-multi-image-kontext-pro.md) | `POST /v1/multi-image-kontext-pro` | [docs](https://www.segmind.com/models/multi-image-kontext-pro/api) |
| [Run MyShell TTS](actions/run-myshell-tts.md) | `POST /v1/myshell-tts` | [docs](https://www.segmind.com/models/myshell-tts/api) |
| [Run Nano Banana](actions/run-nano-banana.md) | `POST /v1/nano-banana` | [docs](https://www.segmind.com/pixelflows/all/nano-banana) |
| [Run Nano Banana 2](actions/run-nano-banana-2.md) | `POST /v1/nano-banana-2` | [docs](https://www.segmind.com/pixelflows/all/nano-banana-2-workflows) |
| [Run Nano Banana Pro](actions/run-nano-banana-pro.md) | `POST /v1/nano-banana-pro` | [docs](https://www.segmind.com/pixelflows/all/nano-banana-pro-workflows) |
| [Run P Image](actions/run-p-image.md) | `POST /v1/p-image` | [docs](https://www.segmind.com/models/p-image/api) |
| [Run P Image Edit](actions/run-p-image-edit.md) | `POST /v1/p-image-edit` | [docs](https://www.segmind.com/models/p-image-edit/api) |
| [Run Pixverse 4.5 Effects](actions/run-pixverse-4-5-effects.md) | `POST /v1/pixverse-4.5-effects` | [docs](https://www.segmind.com/models/pixverse-4.5-effects/api) |
| [Run Pixverse 4.5 Transition](actions/run-pixverse-4-5-transition.md) | `POST /v1/pixverse-4.5-transition` | [docs](https://www.segmind.com/models/pixverse-4.5-transition/api) |
| [Run Pixverse 4.5 Video](actions/run-pixverse-4-5-video.md) | `POST /v1/pixverse-4.5-video` | [docs](https://www.segmind.com/models/pixverse-4.5-video/api) |
| [Run Pixverse 5 Extend](actions/run-pixverse-5-extend.md) | `POST /v1/pixverse-5-extend` | [docs](https://www.segmind.com/models/pixverse-5-extend/api) |
| [Run Pixverse 5 Transition](actions/run-pixverse-5-transition.md) | `POST /v1/pixverse-5-transition` | [docs](https://www.segmind.com/models/pixverse-5-transition/api) |
| [Run Pixverse 5 Video](actions/run-pixverse-5-video.md) | `POST /v1/pixverse-5-video` | [docs](https://www.segmind.com/models/pixverse-5-video/api) |
| [Run Pixverse Image to Video](actions/run-pixverse-image2video.md) | `POST /v1/pixverse-image2video` | [docs](https://www.segmind.com/models/pixverse-image2video/api) |
| [Run Pixverse Text to Video](actions/run-pixverse-text2video.md) | `POST /v1/pixverse-text2video` | [docs](https://www.segmind.com/models/pixverse-text2video/api) |
| [Run Pixverse Transition](actions/run-pixverse-transition.md) | `POST /v1/pixverse-transition` | [docs](https://www.segmind.com/models/pixverse-transition/api) |
| [Run Pixverse V6](actions/run-pixverse-v6.md) | `POST /v1/pixverse-v6` | [docs](https://www.segmind.com/models/pixverse-v6/api) |
| [Run Qwen Image](actions/run-qwen-image.md) | `POST /v1/qwen-image` | [docs](https://www.segmind.com/pixelflows/all/qwen) |
| [Run Qwen Image Edit](actions/run-qwen-image-edit.md) | `POST /v1/qwen-image-edit` | [docs](https://www.segmind.com/models/qwen-image-edit/api) |
| [Run Recraft V3](actions/run-recraft-v3.md) | `POST /v1/recraft-v3` | [docs](https://www.segmind.com/models/recraft-v3/api) |
| [Run Runway Gen4 Turbo](actions/run-runway-gen4-turbo.md) | `POST /v1/runway-gen4-turbo` | [docs](https://www.segmind.com/models/runway-gen4-turbo/api) |
| [Run Seedance Pro](actions/run-seedance-pro.md) | `POST /v1/seedance-pro` | [docs](https://www.segmind.com/pixelflows/all/seedance-pro-workflows) |
| [Run Seedream 4](actions/run-seedream-4.md) | `POST /v1/seedream-4` | [docs](https://www.segmind.com/pixelflows/all/seedream-4-workflows) |
| [Run Sora 2](actions/run-sora-2.md) | `POST /v1/sora-2` | [docs](https://www.segmind.com/models/sora-2/api) |
| [Run Veo 2](actions/run-veo-2.md) | `POST /v1/veo-2` | [docs](https://www.segmind.com/models/veo-2/api) |
| [Run Veo 3](actions/run-veo-3.md) | `POST /v1/veo-3` | [docs](https://www.segmind.com/pixelflows/all/veo-3-workflows) |
| [Run Wan 2.2 I2V Fast](actions/run-wan-2-2-i2v-fast.md) | `POST /v1/wan-2.2-i2v-fast` | [docs](https://www.segmind.com/pixelflows/all/wan-2-2-i2v-fast-workflows) |
| [Run Wan 2.2 T2V Fast](actions/run-wan-2-2-t2v-fast.md) | `POST /v1/wan-2.2-t2v-fast` | [docs](https://www.segmind.com/models/wan-2.2-t2v-fast/api) |
| [Update Dedicated Endpoint](actions/update-dedicated-endpoint.md) | `PUT https://api.spotprod.segmind.com/endpoint/update` | [docs](https://docs.segmind.com/dedicated-endpoints/endpoint-apis) |
| [Upload Asset](actions/upload-asset.md) | `POST https://workflows-api.segmind.com/upload-asset` | [docs](https://docs.segmind.com/api-reference/segmind-storage) |
