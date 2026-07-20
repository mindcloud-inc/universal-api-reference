# <img src="https://images.mindcloud.co/apps/icons/pirsonal_1776788051515.png" alt="Pirsonal logo" width="28" height="28"> Pirsonal: Universal API

Pirsonal is a cloud video personalization and rendering platform for creating templates, generating personalized videos, managing media, and retrieving video outputs through its JSON-RPC API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pirsonal/latest
- **Category:** Communication / Video Communications
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.pirsonal.com
- **Vendor API docs:** https://app.pirsonal.com/docAPI

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Media

| Action | Method | Description |
| --- | --- | --- |
| [Apply Media Pattern](actions/apply-media-pattern.md) | PUT | Applies a pattern to existing media in Pirsonal. |
| [Delete Media](actions/delete-media.md) | DELETE | Deletes an existing media item from Pirsonal. |
| [List Media](actions/list-media.md) | GET | Retrieves media items from your Pirsonal account. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Pirsonal. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from Pirsonal. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from your Pirsonal account. |
| [Set Template Status](actions/set-template-status.md) | PUT | Updates the status of an existing template in Pirsonal. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Pirsonal. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Create Video From Template](actions/create-video-from-template.md) | POST | Creates a new video from a Pirsonal template. |
| [Delete Video](actions/delete-video.md) | DELETE | Deletes an existing video from Pirsonal. |
| [Get Video](actions/get-video.md) | GET | Retrieves video details from your Pirsonal account. |
| [List Template Videos](actions/list-template-videos.md) | GET | Retrieves videos created from a Pirsonal template. |
| [Update Video](actions/update-video.md) | PUT | Updates an existing video in your Pirsonal account. |
| [Update Video Metadata](actions/update-video-metadata.md) | PUT | Updates metadata for an existing video in Pirsonal. |

### Video Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Pirsonal Video Link](actions/get-pirsonal-video-link.md) | GET | Retrieves a downloadable Pirsonal link for a video. |
| [List Video Links](actions/list-video-links.md) | GET | Retrieves downloadable links for a Pirsonal video. |

