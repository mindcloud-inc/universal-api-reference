# <img src="https://images.mindcloud.co/apps/icons/deep-image_1774297503978.png" alt="DeepImage logo" width="28" height="28"> DeepImage: Universal API

DeepImage: Enhance, upscale, and transform images

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deepImage/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://deep-image.ai/
- **Vendor API docs:** https://documentation.deep-image.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves your account information from DeepImage. |

### Image Processing Job

| Action | Method | Description |
| --- | --- | --- |
| [Accurate Business Avatar](actions/accurate-business-avatar.md) | POST | Creates an accurate business avatar in DeepImage. |
| [Auto Enhance Flux2 Klein 9B](actions/auto-enhance-flux2-klein9b.md) | POST | Creates an image with Auto Enhance Klein 9B in DeepImage. |
| [Auto Enhance Generative](actions/auto-enhance-generative.md) | POST | Creates a generatively enhanced image in DeepImage. |
| [Auto Enhance Pro](actions/auto-enhance-pro.md) | POST | Creates an image with Auto Enhance Pro in DeepImage. |
| [Auto Enhance Qwen](actions/auto-enhance-qwen.md) | POST | Creates an image with Auto Enhance Qwen in DeepImage. |
| [Business Avatar Generation](actions/business-avatar-generation.md) | POST | Creates a business avatar image in DeepImage. |
| [Doodle to Image](actions/doodle-to-image.md) | POST | Creates an image from a doodle in DeepImage. |
| [Face Swap](actions/face-swap.md) | POST | Creates a face-swapped image in DeepImage. |
| [Generate Product Scene (Blended)](actions/generate-product-scene-blended.md) | POST | Creates a blended product scene in DeepImage. |
| [Generate Product Scene (Fully Generative)](actions/generate-product-scene-fully-generative.md) | POST | Creates a fully generative product scene in DeepImage. |
| [Generative Upscale](actions/generative-upscale.md) | POST | Creates a generatively upscaled image in DeepImage. |
| [Inpainting / Outpainting](actions/inpainting-outpainting.md) | POST | Creates an inpainted or outpainted image in DeepImage. |
| [Prompt-Based Image Editing](actions/prompt-based-image-editing.md) | POST | Creates an edited image from a prompt in DeepImage. |
| [Storage-to-Storage Processing](actions/storage-to-storage-processing.md) | POST | Queues storage-to-storage image processing in DeepImage. |
| [Text-to-Image Generation](actions/text-to-image-generation.md) | POST | Creates an image from text in DeepImage. |

### Processed Image

| Action | Method | Description |
| --- | --- | --- |
| [Add Caption Overlay](actions/add-caption-overlay.md) | POST | Creates an image with caption overlay in DeepImage. |
| [Auto Enhance Image Quality](actions/auto-enhance-image-quality.md) | POST | Creates an auto-enhanced image in DeepImage. |
| [Clean Image Artifacts](actions/clean-image-artifacts.md) | POST | Creates an artifact-cleaned image in DeepImage. |
| [Correct Exposure](actions/correct-exposure.md) | POST | Creates an image with corrected exposure in DeepImage. |
| [Correct White Balance](actions/correct-white-balance.md) | POST | Creates an image with corrected white balance in DeepImage. |
| [Deblur Image](actions/deblur-image.md) | POST | Creates a deblurred image in DeepImage. |
| [Denoise Image](actions/denoise-image.md) | POST | Creates a denoised image in DeepImage. |
| [Enhance Colors](actions/enhance-colors.md) | POST | Creates an image with enhanced colors in DeepImage. |
| [Enhance Face Details](actions/enhance-face-details.md) | POST | Creates an image with enhanced face details in DeepImage. |
| [Enhance Lighting](actions/enhance-lighting.md) | POST | Creates an image with enhanced lighting in DeepImage. |
| [Prepare for Print](actions/prepare-for-print.md) | POST | Creates a print-ready image in DeepImage. |
| [Process Image and Return Result](actions/process-image-and-return-result.md) | POST | Processes an image and returns the result from DeepImage. |
| [Product Photo Unification](actions/product-photo-unification.md) | POST | Creates a unified product photo in DeepImage. |
| [Remove Background (Auto)](actions/remove-background-auto.md) | POST | Creates an image with background removed automatically in DeepImage. |
| [Remove Background (Human)](actions/remove-background-human.md) | POST | Creates an image with human background removal in DeepImage. |
| [Remove Background (Item)](actions/remove-background-item.md) | POST | Creates an image with item background removal in DeepImage. |
| [Replace Background with Backdrop Image](actions/replace-background-with-backdrop-image.md) | POST | Creates an image with a backdrop background in DeepImage. |
| [Replace Background with Solid Color](actions/replace-background-with-solid-color.md) | POST | Creates an image with a solid-color background in DeepImage. |
| [Resize to Exact Dimensions](actions/resize-to-exact-dimensions.md) | POST | Creates a resized image to exact dimensions in DeepImage. |
| [Smart Content Crop](actions/smart-content-crop.md) | POST | Creates a smart-cropped image in DeepImage. |
| [Upscale by Percentage](actions/upscale-by-percentage.md) | POST | Creates an upscaled image by percentage in DeepImage. |

### Processing Job

| Action | Method | Description |
| --- | --- | --- |
| [Delete Completed Job](actions/delete-completed-job.md) | DELETE | Deletes a completed processing job from DeepImage. |
| [Get Processing Job Result](actions/get-processing-job-result.md) | GET | Retrieves a completed processing job result from DeepImage. |
| [Queue Image Processing Job](actions/queue-image-processing-job.md) | POST | Queues an image processing job in DeepImage. |

