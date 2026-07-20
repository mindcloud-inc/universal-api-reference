# <img src="https://images.mindcloud.co/apps/icons/duply_1774896071871.png" alt="Duply logo" width="28" height="28"> Duply: Universal API

Generate images and videos from reusable templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/duply/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://duply.co/
- **Vendor API docs:** https://app.duply.co/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/duply/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Test Authentication](actions/test-authentication.md) | GET | Tests the connected Duply API credentials. |

### Generated Image

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | POST | Creates a generated image from a Duply template. |
| [Get Generated Image Detail](actions/get-generated-image-detail.md) | GET | Retrieves details for a generated image from Duply. |
| [List Generated Images](actions/list-generated-images.md) | GET | Retrieves your generated images from Duply. |

### Generated Video

| Action | Method | Description |
| --- | --- | --- |
| [Generate Video](actions/generate-video.md) | POST | Creates a generated video from a Duply template. |
| [Get Generated Video Detail](actions/get-generated-video-detail.md) | GET | Retrieves details for a generated video from Duply. |
| [List Generated Videos](actions/list-generated-videos.md) | GET | Retrieves your generated videos from Duply. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Detail](actions/get-template-detail.md) | GET | Retrieves details for a Duply template. |
| [List My Templates](actions/list-my-templates.md) | GET | Retrieves your saved templates from Duply. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves your current usage from Duply. |

