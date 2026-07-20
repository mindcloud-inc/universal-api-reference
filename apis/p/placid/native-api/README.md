# Placid: Native API Reference

A consolidated summary of Placid's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://placid.app/docs/2.0/introduction
- **API base URL:** `https://api.placid.app`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://placid.app/docs/2.0/rest/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | `POST /api/rest/collections` | [docs](https://placid.app/docs/2.0/rest/collections#create) |
| [Create Image](actions/create-image.md) | `POST /api/rest/images` | [docs](https://placid.app/docs/2.0/rest/images#create) |
| [Create PDF](actions/create-pdf.md) | `POST /api/rest/pdfs` | [docs](https://placid.app/docs/2.0/rest/pdfs#create) |
| [Create Template](actions/create-template.md) | `POST /api/rest/templates` | [docs](https://placid.app/docs/2.0/rest/templates#create) |
| [Create Video](actions/create-video.md) | `POST /api/rest/videos` | [docs](https://placid.app/docs/2.0/rest/videos#create) |
| [Delete Collection](actions/delete-collection.md) | `DELETE /api/rest/collections/:collectionId` | [docs](https://placid.app/docs/2.0/rest/collections#delete) |
| [Delete Image](actions/delete-image.md) | `DELETE /api/rest/images/:imageId` | [docs](https://placid.app/docs/2.0/rest/images#delete) |
| [Delete PDF](actions/delete-pdf.md) | `DELETE /api/rest/pdfs/:pdfId` | [docs](https://placid.app/docs/2.0/rest/pdfs#delete) |
| [Delete Template](actions/delete-template.md) | `DELETE /api/rest/templates/:templateUuid` | [docs](https://placid.app/docs/2.0/rest/templates#delete) |
| [Delete Video](actions/delete-video.md) | `DELETE /api/rest/videos/:videoId` | [docs](https://placid.app/docs/2.0/rest/videos#delete) |
| [Get Collection](actions/get-collection.md) | `GET /api/rest/collections/:collectionId` | [docs](https://placid.app/docs/2.0/rest/collections#show) |
| [Get Image](actions/get-image.md) | `GET /api/rest/images/:imageId` | [docs](https://placid.app/docs/2.0/rest/images#show) |
| [Get PDF](actions/get-pdf.md) | `GET /api/rest/pdfs/:pdfId` | [docs](https://placid.app/docs/2.0/rest/pdfs#show) |
| [Get Template](actions/get-template.md) | `GET /api/rest/templates/:templateUuid` | [docs](https://placid.app/docs/2.0/rest/templates#show) |
| [Get Video](actions/get-video.md) | `GET /api/rest/videos/:videoId` | [docs](https://placid.app/docs/2.0/rest/videos#show) |
| [List Collections](actions/list-collections.md) | `GET /api/rest/collections` | [docs](https://placid.app/docs/2.0/rest/collections#index) |
| [List Templates](actions/list-templates.md) | `GET /api/rest/templates` | [docs](https://placid.app/docs/2.0/rest/templates#index) |
| [Merge PDFs](actions/merge-pdfs.md) | `POST /api/rest/pdfs/merge` | [docs](https://placid.app/docs/2.0/rest/pdfs#merge) |
| [Update Collection](actions/update-collection.md) | `PATCH /api/rest/collections/:collectionId` | [docs](https://placid.app/docs/2.0/rest/collections#update) |
| [Update Template](actions/update-template.md) | `PATCH /api/rest/templates/:templateUuid` | [docs](https://placid.app/docs/2.0/rest/templates#update) |
| [Upload Media](actions/upload-media.md) | `POST /api/rest/media` | [docs](https://placid.app/docs/2.0/rest/media) |
