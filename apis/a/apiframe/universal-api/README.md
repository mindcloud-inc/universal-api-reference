# <img src="https://images.mindcloud.co/apps/icons/apiframe_1775080150780.png" alt="Apiframe logo" width="28" height="28"> Apiframe: Universal API

Unified AI generation API for image, video, audio, and media-upload workflows across Midjourney, Ideogram, Flux, Luma, Suno, Udio, and related Apiframe endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/apiframe/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.apiframe.pro
- **Vendor API docs:** https://docs.apiframe.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Upload Audio](actions/upload-audio.md) | POST | Uploads audio to Apiframe and returns a song task ID and URL. |
| [Upload Image](actions/upload-image.md) | POST | Uploads an image to Apiframe and returns its URL. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves your Apiframe account details and credits. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Blend Images](actions/blend-images.md) | POST | Creates an image blending task in Apiframe. |
| [Create Image Variations](actions/create-image-variations.md) | POST | Creates image variations from a previous Apiframe task. |
| [Describe Ideogram Image](actions/describe-ideogram-image.md) | POST | Creates an Ideogram image description task in Apiframe. |
| [Extend Luma Video](actions/extend-luma-video.md) | POST | Creates a Luma video extension task in Apiframe. |
| [Extend Suno Song](actions/extend-suno-song.md) | POST | Creates a Suno song extension task in Apiframe. |
| [Extend Video](actions/extend-video.md) | POST | Creates a video extension task in Apiframe. |
| [Generate AI Photos](actions/generate-ai-photos.md) | POST | Creates an AI photo generation task in Apiframe. |
| [Generate Flux Image](actions/generate-flux-image.md) | POST | Creates a Flux image generation task in Apiframe. |
| [Generate Ideogram Image](actions/generate-ideogram-image.md) | POST | Creates an Ideogram image generation task in Apiframe. |
| [Generate Image](actions/generate-image.md) | POST | Creates an image generation task in Apiframe. |
| [Generate Image Prompts](actions/generate-image-prompts.md) | POST | Creates four image prompts from an image in Apiframe. |
| [Generate Luma Video](actions/generate-luma-video.md) | POST | Creates a Luma video generation task in Apiframe. |
| [Generate Suno Song](actions/generate-suno-song.md) | POST | Creates a Suno song generation task in Apiframe. |
| [Generate Udio Song](actions/generate-udio-song.md) | POST | Creates a Udio song generation task in Apiframe. |
| [Generate Video](actions/generate-video.md) | POST | Creates a video generation task in Apiframe. |
| [Get Image Seed](actions/get-image-seed.md) | GET | Retrieves an Apiframe image seed by task ID. |
| [Get Task Result](actions/get-task-result.md) | GET | Retrieves an Apiframe task result by task ID. |
| [Get Task Results](actions/get-task-results.md) | GET | Retrieves multiple Apiframe task results by task IDs. |
| [Outpaint Image](actions/outpaint-image.md) | POST | Creates an image outpainting task in Apiframe. |
| [Pan Image](actions/pan-image.md) | POST | Creates an image panning task in Apiframe. |
| [Redraw Image Region](actions/redraw-image-region.md) | POST | Creates an image region redraw task in Apiframe. |
| [Remix Ideogram Image](actions/remix-ideogram-image.md) | POST | Creates an Ideogram remix task in Apiframe. |
| [Reroll Images](actions/reroll-images.md) | POST | Creates rerolled images from a previous Apiframe task. |
| [Swap Face](actions/swap-face.md) | POST | Creates a face swap task in Apiframe. |
| [Train AI Photo Model](actions/train-ai-photo-model.md) | POST | Creates an AI photo training task in Apiframe. |
| [Upload and Prepare Training Images](actions/upload-and-prepare-training-images.md) | POST | Uploads and prepares AI photo training images in Apiframe. |
| [Upscale Ideogram Image](actions/upscale-ideogram-image.md) | POST | Creates an Ideogram image upscale task in Apiframe. |

