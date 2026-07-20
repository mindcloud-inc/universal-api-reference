# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-30-174213_1774903364744.png" alt="VisionFly logo" width="28" height="28"> VisionFly: Universal API

Upload, transform, and generate responsive image source sets with VisionFly's image optimization API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/visionFly/latest
- **Category:** Content & Files / Storage
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://visionfly.ai
- **Vendor API docs:** https://api.visionfly.ai/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test API Key](actions/test-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/test-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Api

| Action | Method | Description |
| --- | --- | --- |
| [Get Root Info](actions/get-root-info.md) | GET | Retrieves API details from VisionFly. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Test API Key](actions/test-api-key.md) | GET | Retrieves authentication details from VisionFly. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Delete Image from CDN](actions/delete-image-from-cdn.md) | DELETE | Deletes an image from the VisionFly CDN. |
| [Delete Multiple Images](actions/delete-multiple-images.md) | DELETE | Deletes multiple images from the VisionFly CDN. |
| [List User Images](actions/list-user-images.md) | GET | Retrieves user images from the VisionFly CDN. |
| [Serve CDN Image](actions/serve-cdn-image.md) | GET | Retrieves an image from the VisionFly CDN. |
| [Upload Image to CDN](actions/upload-image-to-cdn.md) | POST | Uploads an image to the VisionFly CDN. |

### Passport Specs

| Action | Method | Description |
| --- | --- | --- |
| [Get Passport Photo Specifications](actions/get-passport-photo-specifications.md) | GET | Retrieves passport photo specifications from VisionFly. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get Plans](actions/get-plans.md) | GET | Retrieves subscription plans from VisionFly. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from VisionFly. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves the current service status from VisionFly. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage Statistics](actions/get-usage-statistics.md) | GET | Retrieves usage statistics from VisionFly. |

