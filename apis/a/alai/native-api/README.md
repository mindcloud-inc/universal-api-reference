# Alai: Native API Reference

A consolidated summary of Alai's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.getalai.com/api/introduction
- **API base URL:** `https://slides-api.getalai.com/api/v1`

## Authentication

### API Key

Connect your Alai account with an API key generated from Alai settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.getalai.com/api/get-themes)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Slide](actions/create-slide.md) | `POST /presentations/:presentation_id/slides` | [docs](https://docs.getalai.com/api/create-slide) |
| [Delete Presentation](actions/delete-presentation.md) | `DELETE /presentations/:presentation_id` | [docs](https://docs.getalai.com/api/delete-presentation) |
| [Delete Slide](actions/delete-slide.md) | `DELETE /presentations/:presentation_id/slides/:slide_id` | [docs](https://docs.getalai.com/api/delete-slide) |
| [Export Presentation](actions/export-presentation.md) | `POST /presentations/:presentation_id/exports` | [docs](https://docs.getalai.com/api/export-presentation) |
| [Extract Transcripts](actions/extract-transcripts.md) | `POST /presentations/:presentation_id/transcripts` | [docs](https://docs.getalai.com/api/generate-transcripts) |
| [Generate Presentation](actions/generate-presentation.md) | `POST /generations` | [docs](https://docs.getalai.com/api/generations) |
| [Get Generation Status](actions/get-generation-status.md) | `GET /generations/:generation_id` | [docs](https://docs.getalai.com/api/generation-status) |
| [List Presentations](actions/list-presentations.md) | `GET /presentations` | [docs](https://docs.getalai.com/api/get-presentations) |
| [List Themes](actions/list-themes.md) | `GET /themes` | [docs](https://docs.getalai.com/api/get-themes) |
| [Upload Images](actions/upload-images.md) | `POST /upload-images` | [docs](https://docs.getalai.com/api/upload-images) |
| [Verify API Key](actions/verify-api-key.md) | `GET /ping` | [docs](https://docs.getalai.com/api/introduction) |
