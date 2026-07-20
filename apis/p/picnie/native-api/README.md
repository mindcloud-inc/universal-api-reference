# Picnie: Native API Reference

A consolidated summary of Picnie's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://docs.picnie.com/api-reference/api-overview-rl61
- **API base URL:** `https://picnie.com/api/v1`

## Authentication

### API Key

Connect Picnie with your API key from Account -> API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.picnie.com/api-reference/api-overview-rl61)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Image Watermark](actions/add-image-watermark.md) | `POST /add-watermark-image` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Add Text Watermark](actions/add-text-watermark.md) | `POST /add-watermark-text-on-image` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Apply Image Filter](actions/apply-image-filter.md) | `POST /filter-on-image` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Compress Image](actions/compress-image.md) | `POST /compress-image` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Convert Image](actions/convert-image.md) | `POST /convert-image` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Create Image](actions/create-image.md) | `POST /create-image` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Create Image Collection](actions/create-image-collection.md) | `POST /create-image-collection` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Create PDF](actions/create-pdf.md) | `POST /create-pdf` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Create Project](actions/create-project.md) | `POST /create-project` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Crop Image](actions/crop-image.md) | `POST /crop-image` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Get Image Metadata](actions/get-image-metadata.md) | `POST /get-image-metadata` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Get Template](actions/get-template.md) | `POST /get-template` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [List Projects](actions/list-projects.md) | `POST /get-my-projects` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [List Templates](actions/list-templates.md) | `POST /get-my-templates` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Remove Background](actions/remove-background.md) | `POST /remove-background` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Resize Image](actions/resize-image.md) | `POST /resize-image` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Transcribe Image](actions/transcribe-image.md) | `POST /transcribe-image` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
| [Upload Asset](actions/upload-asset.md) | `POST /upload-asset` | [docs](https://documenter.getpostman.com/view/25712226/2s93CGRvy6) |
