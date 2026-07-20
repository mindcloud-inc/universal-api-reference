# <img src="https://images.mindcloud.co/apps/icons/images-27_1774890673025.png" alt="BHuman logo" width="28" height="28"> BHuman: Universal API

BHuman public API for managing video instances, generation jobs, workspaces, and store resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bHuman/latest
- **Category:** Communication / Video Communications
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bhuman.ai
- **Vendor API docs:** https://github.com/bhuman-ai/public_api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Generated Video

| Action | Method | Description |
| --- | --- | --- |
| [Generate Video by Campaign](actions/generate-video-by-campaign.md) | POST | Creates personalized videos from a campaign in BHuman. |
| [Generate Video by Instance](actions/generate-video-by-instance.md) | POST | Creates personalized videos from a video instance in BHuman. |
| [Get Generated Video](actions/get-generated-video.md) | GET | Retrieves a generated video from BHuman. |
| [List Generated Videos by Campaign](actions/list-generated-videos-by-campaign.md) | GET | Retrieves generated videos for a campaign in BHuman. |
| [List Generated Videos by Instance](actions/list-generated-videos-by-instance.md) | GET | Retrieves generated videos for a video instance in BHuman. |

### Store Product

| Action | Method | Description |
| --- | --- | --- |
| [List Store Products](actions/list-store-products.md) | GET | Retrieves available store products from BHuman. |
| [Use Store Product](actions/use-store-product.md) | POST | Creates a video instance from a store product in BHuman. |

### Store Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Store Settings](actions/get-store-settings.md) | GET | Retrieves store categories and tags from BHuman. |

### Video Instance

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Instance](actions/get-video-instance.md) | GET | Retrieves an AI Studio video instance from BHuman. |
| [List Video Instances](actions/list-video-instances.md) | GET | Retrieves AI Studio video instances from BHuman. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves available account workspaces from BHuman. |

