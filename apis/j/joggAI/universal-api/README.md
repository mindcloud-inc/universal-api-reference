# <img src="https://images.mindcloud.co/apps/icons/joggai_1774986027639.png" alt="JoggAI logo" width="28" height="28"> JoggAI: Universal API

Create AI avatar videos, templates, assets, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/joggAI/latest
- **Category:** Marketing
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.jogg.ai
- **Vendor API docs:** https://docs.jogg.ai/api-reference/v2/QuickStart/GettingStarted

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Ai Script Result

| Action | Method | Description |
| --- | --- | --- |
| [Get AI Script Results](actions/get-ai-script-results.md) | GET |  |

### Ai Script Task

| Action | Method | Description |
| --- | --- | --- |
| [Generate AI Scripts](actions/generate-ai-scripts.md) | POST |  |

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Upload Asset](actions/upload-asset.md) | POST |  |

### Avatar

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Avatars](actions/list-custom-avatars.md) | GET |  |
| [List Public Avatars](actions/list-public-avatars.md) | GET |  |

### Avatar Video

| Action | Method | Description |
| --- | --- | --- |
| [Create Video From Avatar](actions/create-video-from-avatar.md) | POST |  |
| [Get Avatar Video Status](actions/get-avatar-video-status.md) | GET |  |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Translation Target Languages](actions/list-translation-target-languages.md) | GET |  |

### Lip Sync Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Lip Sync Video Task](actions/create-lip-sync-video-task.md) | POST |  |

### Motion

| Action | Method | Description |
| --- | --- | --- |
| [Get Motion Status](actions/get-motion-status.md) | GET |  |

### Music

| Action | Method | Description |
| --- | --- | --- |
| [List Background Music](actions/list-background-music.md) | GET |  |

### Photo

| Action | Method | Description |
| --- | --- | --- |
| [Create Photo Avatar](actions/create-photo-avatar.md) | POST |  |
| [Get Photo Avatar Status](actions/get-photo-avatar-status.md) | GET |  |
| [List Photo Avatars](actions/list-photo-avatars.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Product Video

| Action | Method | Description |
| --- | --- | --- |
| [Create Video From Product](actions/create-video-from-product.md) | POST |  |

### Quota

| Action | Method | Description |
| --- | --- | --- |
| [Get Remaining Quota](actions/get-remaining-quota.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET |  |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Create Video with Template](actions/create-video-with-template.md) | POST |  |
| [Get Template Video](actions/get-template-video.md) | GET |  |

### Video Translation

| Action | Method | Description |
| --- | --- | --- |
| [Get Translation Status](actions/get-translation-status.md) | GET |  |
| [Translate Video](actions/translate-video.md) | POST |  |

### Visual Style

| Action | Method | Description |
| --- | --- | --- |
| [List Visual Styles](actions/list-visual-styles.md) | GET |  |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Voices](actions/list-custom-voices.md) | GET |  |
| [List Voices](actions/list-voices.md) | GET |  |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | POST |  |
| [Delete Webhook Endpoint](actions/delete-webhook-endpoint.md) | DELETE |  |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET |  |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Events](actions/list-webhook-events.md) | GET |  |

