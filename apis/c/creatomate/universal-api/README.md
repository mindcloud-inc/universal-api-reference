# <img src="https://images.mindcloud.co/apps/icons/creatomate_1773694181966.png" alt="Creatomate logo" width="28" height="28"> Creatomate: Universal API

Create, render, and manage automated videos and images

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/creatomate/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://creatomate.com
- **Vendor API docs:** https://creatomate.com/docs/api/reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Render Status](actions/get-render-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/get-render-status?connectionId=$CONNECTION_ID&renderId=c4f6d4f1-7a4e-4b67-9f90-3fc76f3c7d0e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Render

| Action | Method | Description |
| --- | --- | --- |
| [Concatenate Multiple Videos](actions/concatenate-multiple-videos.md) | POST | Creates a concatenated video render in Creatomate. |
| [Distribute Elements Over Time](actions/distribute-elements-over-time.md) | POST | Creates a render that distributes elements over time. |
| [Generate Image Slideshow](actions/generate-image-slideshow.md) | POST | Creates an image slideshow render in Creatomate. |
| [Generate Voiceover Video](actions/generate-voiceover-video.md) | POST | Creates a voiceover video render in Creatomate. |
| [Generate Voiceover Video With Captions](actions/generate-voiceover-video-with-captions.md) | POST | Creates a voiceover video with captions in Creatomate. |
| [Group Elements Into Scenes](actions/group-elements-into-scenes.md) | POST | Creates a render that groups elements into scenes. |
| [Inject RenderScript Into Template](actions/inject-render-script-into-template.md) | POST | Creates a render by injecting RenderScript into a template. |
| [Rearrange Scenes In Template](actions/rearrange-scenes-in-template.md) | POST | Creates a render with rearranged template scenes in Creatomate. |
| [Synchronize Multiple Elements](actions/synchronize-multiple-elements.md) | POST | Creates a render that synchronizes multiple elements. |
| [Use A Custom Font](actions/use-a-custom-font.md) | POST | Creates a render that uses a custom font. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves all templates from Creatomate. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template By ID](actions/get-template-by-id.md) | GET | Retrieves a template from Creatomate. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Image From Template](actions/create-image-from-template.md) | POST | Creates an image render from a template in Creatomate. |
| [Create Render](actions/create-render.md) | POST | Creates a new render in Creatomate. |
| [Create Render From RenderScript](actions/create-render-from-render-script.md) | POST | Creates a render from RenderScript in Creatomate. |
| [Create Render With Metadata](actions/create-render-with-metadata.md) | POST | Creates a render with metadata in Creatomate. |
| [Create Render With Render Scale](actions/create-render-with-render-scale.md) | POST | Creates a render with render scale in Creatomate. |
| [Create Render With Size Constraints](actions/create-render-with-size-constraints.md) | POST | Creates a render with size constraints in Creatomate. |
| [Create Render With Template Modifications](actions/create-render-with-template-modifications.md) | POST | Creates a render with template modifications in Creatomate. |
| [Create Render With Webhook Callback](actions/create-render-with-webhook-callback.md) | POST | Creates a render with a webhook callback in Creatomate. |
| [Create Video From Template](actions/create-video-from-template.md) | POST | Creates a video render from a template in Creatomate. |
| [Get Render Status](actions/get-render-status.md) | GET | Retrieves a render's status from Creatomate. |

