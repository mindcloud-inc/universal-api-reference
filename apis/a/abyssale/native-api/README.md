# Abyssale: Native API Reference

A consolidated summary of Abyssale's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://developers.abyssale.com/
- **API base URL:** `https://api.abyssale.com`

## Authentication

### API Key

Authenticate with an Abyssale workspace API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://help.abyssale.com/en/articles/329008-how-to-create-and-manage-your-abyssale-api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Banner Export ZIP](actions/create-banner-export-zip.md) | `POST /async/banners/export` | [docs](https://developers.abyssale.com/rest-api/image-export) |
| [Create Dynamic Image URL](actions/create-dynamic-image-url.md) | `POST /designs/:designId/dynamic-image-url` | [docs](https://developers.abyssale.com/dynamic-images/create-a-dynamic-image-by-api) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://developers.abyssale.com/rest-api/projects) |
| [Duplicate Workspace Template](actions/duplicate-workspace-template.md) | `POST /workspace-templates/:companyTemplateId/use` | [docs](https://developers.abyssale.com/rest-api/workspace-templates) |
| [Duplicate Workspace Template With Custom Name](actions/duplicate-workspace-template-with-custom-name.md) | `POST /workspace-templates/:companyTemplateId/use` | [docs](https://developers.abyssale.com/rest-api/workspace-templates) |
| [Generate All Formats For A Design](actions/generate-all-formats-for-a-design.md) | `POST /async/banner-builder/:design_id/generate` | [docs](https://developers.abyssale.com/rest-api/generation/asynchronous-generation/generate-multi-format-images) |
| [Generate Animated GIFs](actions/generate-animated-gifs.md) | `POST /async/banner-builder/:design_id/generate` | [docs](https://developers.abyssale.com/rest-api/generation/asynchronous-generation/generate-multi-format-animated-gifs) |
| [Generate Async Visual Version](actions/generate-async-visual-version.md) | `POST /async/banner-builder/:design_id/generate` | [docs](https://developers.abyssale.com/rest-api/generation/visual-versioning) |
| [Generate HTML5 Banner Ads](actions/generate-html5-banner-ads.md) | `POST /async/banner-builder/:design_id/generate` | [docs](https://developers.abyssale.com/rest-api/generation/asynchronous-generation/generate-html5-banner-ads) |
| [Generate MP4 Videos](actions/generate-mp4-videos.md) | `POST /async/banner-builder/:design_id/generate` | [docs](https://developers.abyssale.com/rest-api/generation/asynchronous-generation/generate-multi-format-videos) |
| [Generate Multi-Page Printable PDF](actions/generate-multi-page-printable-pdf.md) | `POST /async/banner-builder/:design_id/generate` | [docs](https://developers.abyssale.com/rest-api/generation/asynchronous-generation/generate-multi-page-pdf-for-printing) |
| [Generate New Visual Version](actions/generate-new-visual-version.md) | `POST /banner-builder/:designId/generate` | [docs](https://developers.abyssale.com/rest-api/generation/visual-versioning) |
| [Generate Printable PDF Batch](actions/generate-printable-pdf-batch.md) | `POST /async/banner-builder/:design_id/generate` | [docs](https://developers.abyssale.com/rest-api/generation/asynchronous-generation/generate-multi-format-pdfs-for-printing) |
| [Generate Single Image](actions/generate-single-image.md) | `POST /banner-builder/:designId/generate` | [docs](https://developers.abyssale.com/rest-api/generation/synchronous-generation/generate-single-image) |
| [Get Design Details](actions/get-design-details.md) | `GET /designs/:designId` | [docs](https://developers.abyssale.com/rest-api/designs/design-details) |
| [Get Design Details Advanced](actions/get-design-details-advanced.md) | `GET /designs/:designId` | [docs](https://developers.abyssale.com/rest-api/designs/design-details) |
| [Get Design Format Details](actions/get-design-format-details.md) | `GET /designs/:designId/formats/:formatSpecifier` | [docs](https://developers.abyssale.com/rest-api/designs/design-format-details) |
| [Get Duplication Request Status](actions/get-duplication-request-status.md) | `GET /design-duplication-requests/:duplicateRequestId` | [docs](https://developers.abyssale.com/rest-api/workspace-templates) |
| [Get File](actions/get-file.md) | `GET /banners/:bannerId` | [docs](https://api-reference.abyssale.com/) |
| [Get Fonts](actions/get-fonts.md) | `GET /fonts` | [docs](https://developers.abyssale.com/rest-api/fonts) |
| [List Designs](actions/list-designs.md) | `GET /designs` | [docs](https://developers.abyssale.com/rest-api/designs) |
| [List Designs By Category](actions/list-designs-by-category.md) | `GET /designs` | [docs](https://developers.abyssale.com/rest-api/designs) |
| [List Designs By Type](actions/list-designs-by-type.md) | `GET /designs` | [docs](https://developers.abyssale.com/rest-api/designs) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developers.abyssale.com/rest-api/projects) |
| [Poll Async Generation Request](actions/poll-async-generation-request.md) | `GET /generation-request/:generation_request_id` | [docs](https://developers.abyssale.com/rest-api/generation/asynchronous-generation) |
