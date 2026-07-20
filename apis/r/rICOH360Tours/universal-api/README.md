# <img src="https://images.mindcloud.co/apps/icons/id-gfvf-wk-l-logos_1775677717048.jpeg" alt="RICOH360 Tours logo" width="28" height="28"> RICOH360 Tours: Universal API

Manage RICOH360 tours, teams, and virtual tour data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rICOH360Tours/latest
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ricoh360.com/tours
- **Vendor API docs:** https://docs.ricoh360.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Team By API Key](actions/get-team-by-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/get-team-by-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### 360 Viewer Asset

| Action | Method | Description |
| --- | --- | --- |
| [Get 360 Viewer Asset](actions/get-360-viewer-asset.md) | GET |  |

### Ai Image Enhancement

| Action | Method | Description |
| --- | --- | --- |
| [Run AI Image Enhancement](actions/run-ai-image-enhancement.md) | PUT |  |

### Ai Video

| Action | Method | Description |
| --- | --- | --- |
| [Run AI Video Maker](actions/run-ai-video-maker.md) | POST |  |

### Ai Virtual Staging

| Action | Method | Description |
| --- | --- | --- |
| [Run AI Virtual Staging](actions/run-ai-virtual-staging.md) | POST |  |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Apply Image Blur](actions/apply-image-blur.md) | PUT |  |
| [Generate Cubic Projection](actions/generate-cubic-projection.md) | PUT |  |
| [Generate Thumbnail](actions/generate-thumbnail.md) | PUT |  |
| [Search Media Assets](actions/search-media-assets.md) | GET |  |
| [Select AI Video Source Scenes](actions/select-ai-video-source-scenes.md) | POST |  |
| [Store Media Asset](actions/store-media-asset.md) | POST |  |
| [Sync Device Photos](actions/sync-device-photos.md) | PUT |  |
| [Sync Device Videos](actions/sync-device-videos.md) | PUT |  |

### Auto Image Cropping

| Action | Method | Description |
| --- | --- | --- |
| [Run Auto Image Cropping](actions/run-auto-image-cropping.md) | POST |  |

### Floor Plan

| Action | Method | Description |
| --- | --- | --- |
| [Generate Floor Plan](actions/generate-floor-plan.md) | POST |  |

### Floor Plan Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Floor Plan](actions/export-floor-plan.md) | GET |  |

### Floor Plan Room Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Map Floor Plan Rooms](actions/map-floor-plan-rooms.md) | POST |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Embedded Tour Code](actions/get-embedded-tour-code.md) | GET |  |
| [Get Portal Tour URL](actions/get-portal-tour-url.md) | GET |  |
| [Get Tour Neighbourhood Map](actions/get-tour-neighbourhood-map.md) | GET |  |
| [Publish Virtual Tour](actions/publish-virtual-tour.md) | PUT |  |
| [Reorder Tour Rooms](actions/reorder-tour-rooms.md) | PUT |  |
| [Share Tour To Facebook](actions/share-tour-to-facebook.md) | POST |  |
| [Share Virtual Tour](actions/share-virtual-tour.md) | POST |  |
| [Update Custom Branding](actions/update-custom-branding.md) | PUT |  |
| [Update Virtual Business Card](actions/update-virtual-business-card.md) | PUT |  |

### Scene Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Create Scene Annotation](actions/create-scene-annotation.md) | POST |  |
| [Update Scene Annotation](actions/update-scene-annotation.md) | PUT |  |

### Scene Label

| Action | Method | Description |
| --- | --- | --- |
| [Update Scene Label](actions/update-scene-label.md) | PUT |  |

### Staged Image Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Staged Images](actions/import-staged-images.md) | POST |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team By API Key](actions/get-team-by-api-key.md) | GET |  |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Invite Team Member](actions/invite-team-member.md) | POST |  |
| [List Team Members](actions/list-team-members.md) | GET |  |

### Tour 2d Image

| Action | Method | Description |
| --- | --- | --- |
| [Upload Tour 2D Image](actions/upload-tour-2d-image.md) | POST |  |

### Tour 360 Image

| Action | Method | Description |
| --- | --- | --- |
| [Upload Tour 360 Image](actions/upload-tour-360-image.md) | POST |  |

### Virtual Tour

| Action | Method | Description |
| --- | --- | --- |
| [Create Virtual Tour](actions/create-virtual-tour.md) | POST |  |
| [Get Virtual Tour](actions/get-virtual-tour.md) | GET |  |
| [List Virtual Tours](actions/list-virtual-tours.md) | GET |  |
| [Update Virtual Tour](actions/update-virtual-tour.md) | PUT |  |

### Virtual Tour Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Virtual Tour Analytics](actions/get-virtual-tour-analytics.md) | GET |  |

### Walk-through Path

| Action | Method | Description |
| --- | --- | --- |
| [Create Walk-Through Path](actions/create-walk-through-path.md) | POST |  |
| [Update Walk-Through Path](actions/update-walk-through-path.md) | PUT |  |

