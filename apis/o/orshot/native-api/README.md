# Orshot: Native API Reference

A consolidated summary of Orshot's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://orshot.com/docs/api-reference
- **API base URL:** `https://api.orshot.com/v1`

## Authentication

### API Key

Authenticate with your Orshot API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://orshot.com/docs/quick-start/get-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–20). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Brand Color](actions/add-brand-color.md) | `POST /brand-assets/colors/add` | [docs](https://orshot.com/docs/api-reference/brand-colors-post) |
| [Delete Brand Asset Image](actions/delete-brand-asset-image.md) | `DELETE /brand-assets/images/delete/:id` | [docs](https://orshot.com/docs/api-reference/brand-assets-delete) |
| [Delete Brand Color](actions/delete-brand-color.md) | `DELETE /brand-assets/colors/delete/:id` | [docs](https://orshot.com/docs/api-reference/brand-colors-delete) |
| [Delete Brand Video](actions/delete-brand-video.md) | `DELETE /brand-assets/videos/delete/:id` | [docs](https://orshot.com/docs/api-reference/brand-videos-delete) |
| [Delete Studio Template](actions/delete-studio-template.md) | `DELETE /studio/templates/:templateId/delete` | [docs](https://orshot.com/docs/api-reference/studio-template-delete) |
| [Generate Signed URL](actions/generate-signed-url.md) | `POST /signed-url/create` | [docs](https://orshot.com/docs/api-reference/generate-signed-url) |
| [Get All Studio Templates](actions/get-all-studio-templates.md) | `GET /studio/templates/all` | [docs](https://orshot.com/docs/api-reference/studio-templates-list) |
| [Get Brand Asset Images](actions/get-brand-asset-images.md) | `GET /brand-assets/images/get` | [docs](https://orshot.com/docs/api-reference/brand-assets-get) |
| [Get Brand Colors](actions/get-brand-colors.md) | `GET /brand-assets/colors/get` | [docs](https://orshot.com/docs/api-reference/brand-colors-get) |
| [Get Brand Fonts](actions/get-brand-fonts.md) | `GET /brand-assets/fonts/get` | [docs](https://orshot.com/docs/api-reference/custom-fonts-get) |
| [Get Brand Videos](actions/get-brand-videos.md) | `GET /brand-assets/videos/get` | [docs](https://orshot.com/docs/api-reference/brand-videos-get) |
| [Get Profile and Workspaces](actions/get-profile-and-workspaces.md) | `GET /me` | [docs](https://orshot.com/docs/api-reference/get-profile-workspace) |
| [Get Studio Template](actions/get-studio-template.md) | `GET /studio/templates/:templateId` | [docs](https://orshot.com/docs/api-reference/studio-template-get) |
| [Render from a Utility Template](actions/render-from-a-utility-template.md) | `POST /generate/:renderType` | [docs](https://orshot.com/docs/api-reference/render-from-template) |
| [Render from Studio Template](actions/render-from-studio-template.md) | `POST /studio/render` | [docs](https://orshot.com/docs/api-reference/render-from-studio-template) |
| [Update Brand Asset Image Tags](actions/update-brand-asset-image-tags.md) | `PATCH /brand-assets/images/update/:id` | [docs](https://orshot.com/docs/api-reference/brand-assets-update) |
| [Update Brand Color Tags](actions/update-brand-color-tags.md) | `PATCH /brand-assets/colors/update/:id` | [docs](https://orshot.com/docs/api-reference/brand-colors-update) |
| [Update Brand Video Tags](actions/update-brand-video-tags.md) | `PATCH /brand-assets/videos/update/:id` | [docs](https://orshot.com/docs/api-reference/brand-videos-update) |
| [Upload Brand Asset Image](actions/upload-brand-asset-image.md) | `POST /brand-assets/images/add` | [docs](https://orshot.com/docs/api-reference/brand-assets-post) |
| [Upload Brand Video](actions/upload-brand-video.md) | `POST /brand-assets/videos/add` | [docs](https://orshot.com/docs/api-reference/brand-videos-post) |
