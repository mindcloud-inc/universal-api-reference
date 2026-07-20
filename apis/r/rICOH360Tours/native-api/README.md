# RICOH360 Tours: Native API Reference

A consolidated summary of RICOH360 Tours's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://docs.ricoh360.com/
- **API base URL:** `https://bbomwcm27nhalfwjvwzy6qbrim.appsync-api.us-west-2.amazonaws.com`

## Authentication

### API Key

Connect with a team API key from RICOH360 Tours Team Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.ricoh360.com/hc/en-us/articles/16474419660435-API-Key-Acquisition-Procedure)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Image Blur](actions/apply-image-blur.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/4404305780371--7-29-2021-Blur) |
| [Create Scene Annotation](actions/create-scene-annotation.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360062219334-Creating-Annotations) |
| [Create Virtual Tour](actions/create-virtual-tour.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360058326733-Creating-a-tour) |
| [Create Walk-Through Path](actions/create-walk-through-path.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360056451994-Creating-Tour-Paths) |
| [Export Floor Plan](actions/export-floor-plan.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360062221494-Using-EDIT-Tour-for-Managing-Floor-Plans) |
| [Generate Cubic Projection](actions/generate-cubic-projection.md) | `POST /graphql` | [docs](https://www.ricoh360.com/developer/) |
| [Generate Floor Plan](actions/generate-floor-plan.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/5811061201555--5-12-2022-Floor-Plan-Generator-has-been-released) |
| [Generate Thumbnail](actions/generate-thumbnail.md) | `POST /graphql` | [docs](https://www.ricoh360.com/developer/) |
| [Get 360 Viewer Asset](actions/get-360-viewer-asset.md) | `POST /graphql` | [docs](https://www.ricoh360.com/developer/) |
| [Get Embedded Tour Code](actions/get-embedded-tour-code.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360058327973-Tour-Settings) |
| [Get Portal Tour URL](actions/get-portal-tour-url.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/19169916827283-Custom-Domain-Settings-Changing-Tour-URLs) |
| [Get Team By API Key](actions/get-team-by-api-key.md) | `POST /graphql` | [docs](https://docs.ricoh360.com/) |
| [Get Tour Neighbourhood Map](actions/get-tour-neighbourhood-map.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/18250620879763-Edit-Tour-Info) |
| [Get Virtual Tour](actions/get-virtual-tour.md) | `POST /graphql` | [docs](https://www.ricoh360.com/tours/features/) |
| [Get Virtual Tour Analytics](actions/get-virtual-tour-analytics.md) | `POST /graphql` | [docs](https://www.ricoh360.com/tours/features/) |
| [Import Staged Images](actions/import-staged-images.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/4403388605075-AI-Virtual-Staging) |
| [Invite Team Member](actions/invite-team-member.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360050751253-Team-Overview) |
| [List Team Members](actions/list-team-members.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360050751253-Team-Overview) |
| [List Virtual Tours](actions/list-virtual-tours.md) | `POST /graphql` | [docs](https://www.ricoh360.com/tours/features/) |
| [Map Floor Plan Rooms](actions/map-floor-plan-rooms.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360062221494-Using-EDIT-Tour-for-Managing-Floor-Plans) |
| [Publish Virtual Tour](actions/publish-virtual-tour.md) | `POST /graphql` | [docs](https://www.ricoh360.com/tours/) |
| [Reorder Tour Rooms](actions/reorder-tour-rooms.md) | `POST /graphql` | [docs](https://www.ricoh360.com/tours/features/) |
| [Run AI Image Enhancement](actions/run-ai-image-enhancement.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/17412999356275-AI-Image-Enhancement) |
| [Run AI Video Maker](actions/run-ai-video-maker.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360061734594-AI-Video-Maker) |
| [Run AI Virtual Staging](actions/run-ai-virtual-staging.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/4403388605075-AI-Virtual-Staging) |
| [Run Auto Image Cropping](actions/run-auto-image-cropping.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/19587308817939-Cropping-Your-Panoramas) |
| [Search Media Assets](actions/search-media-assets.md) | `POST /graphql` | [docs](https://www.ricoh360.com/developer/) |
| [Select AI Video Source Scenes](actions/select-ai-video-source-scenes.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360061734594-AI-Video-Maker) |
| [Share Tour To Facebook](actions/share-tour-to-facebook.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360058327033-Sharing-a-tour) |
| [Share Virtual Tour](actions/share-virtual-tour.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360058327033-Sharing-a-tour) |
| [Store Media Asset](actions/store-media-asset.md) | `POST /graphql` | [docs](https://www.ricoh360.com/developer/) |
| [Sync Device Photos](actions/sync-device-photos.md) | `POST /graphql` | [docs](https://www.ricoh360.com/developer/) |
| [Sync Device Videos](actions/sync-device-videos.md) | `POST /graphql` | [docs](https://www.ricoh360.com/developer/) |
| [Update Custom Branding](actions/update-custom-branding.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/1500003038802-Creating-and-Setting-Brand-Banners) |
| [Update Scene Annotation](actions/update-scene-annotation.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360062219334-Creating-Annotations) |
| [Update Scene Label](actions/update-scene-label.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360058327553-Edit-Photo-Name) |
| [Update Virtual Business Card](actions/update-virtual-business-card.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/11956798675603-Specifications-for-Brand-Banner-Business-Card-and-Tripod-Cover) |
| [Update Virtual Tour](actions/update-virtual-tour.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360058326733-Creating-a-tour) |
| [Update Walk-Through Path](actions/update-walk-through-path.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/35196484786323-Change-Walkthrough-settings-when-viewing-tours) |
| [Upload Tour 2D Image](actions/upload-tour-2d-image.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/36828221357971-List-of-Available-Image-Formats-and-Sizes) |
| [Upload Tour 360 Image](actions/upload-tour-360-image.md) | `POST /graphql` | [docs](https://help.ricoh360.com/hc/en-us/articles/360058327913-Adding-photos) |
