# Colossyan: Native API Reference

A consolidated summary of Colossyan's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.colossyan.com
- **OpenAPI specification:** https://docs.colossyan.com/llms.txt
- **API base URL:** `https://app.colossyan.com/api/v1`

## Authentication

### API Key

Bearer token for a Colossyan workspace API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.colossyan.com/basics/editor)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Avatar](actions/create-avatar.md) | `POST /assets/actors` | [docs](https://docs.colossyan.com/avatar-creation/create-avatar) |
| [Create Video From Template](actions/create-video-from-template.md) | `POST /video-generation-jobs/template-jobs` | [docs](https://docs.colossyan.com/video-generation/video-generation/generating-using-a-template) |
| [Create Video Generation Job](actions/create-video-generation-job.md) | `POST /video-generation-jobs` | [docs](https://docs.colossyan.com/video-generation/video-generation/generating-a-video-manually) |
| [Delete Generated Video](actions/delete-generated-video.md) | `DELETE /generated-videos/:videoId` | [docs](https://docs.colossyan.com/video-generation/generated-videos/delete-a-video) |
| [Delete Video Generation Job](actions/delete-video-generation-job.md) | `DELETE /video-generation-jobs/:videoGenerationJobId` | [docs](https://docs.colossyan.com/video-generation/video-generation-job/delete-video-generation-job) |
| [Generate Draft From Knowledge](actions/generate-draft-from-knowledge.md) | `POST https://app.colossyan.com/api/knowledge-to-draft/generate-draft` | [docs](https://docs.colossyan.com/experimental/knowledge-to-draft) |
| [List Avatars](actions/list-avatars.md) | `GET /assets/actors` | [docs](https://docs.colossyan.com/basics/openapi/list-avatars) |
| [List Voices](actions/list-voices.md) | `GET /assets/voices` | [docs](https://docs.colossyan.com/basics/openapi/list-voices) |
| [Retrieve Generated Video](actions/retrieve-generated-video.md) | `GET /generated-videos/:videoId` | [docs](https://docs.colossyan.com/video-generation/generated-videos/retrieve-a-video) |
| [Retrieve Video Generation Job](actions/retrieve-video-generation-job.md) | `GET /video-generation-jobs/:videoGenerationJobId` | [docs](https://docs.colossyan.com/video-generation/video-generation-job/retrieve-video-generation-job) |
