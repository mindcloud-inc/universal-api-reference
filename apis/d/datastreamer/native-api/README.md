# Datastreamer: Native API Reference

A consolidated summary of Datastreamer's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.datastreamer.io/docs/welcome-to-datastreamer
- **API base URL:** `https://api.platform.datastreamer.io`

## Authentication

### API Key

Use a Datastreamer Platform API key from Portal Keys & Secrets.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.datastreamer.io/docs/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `records`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Job DVU Usage](actions/count-job-dvu-usage.md) | `POST /api/v2/customer-usage/jobs` | [docs](https://docs.datastreamer.io/docs/jobs-dvu-count-api) |
| [Create Bluesky Live Feed Job](actions/create-bluesky-live-feed-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/bluesky-live-feed) |
| [Create DarkOwl Search Job](actions/create-dark-owl-search-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/darkowl-search) |
| [Create Data365 Facebook Posts Search Job](actions/create-data365-facebook-posts-search-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/data365-facebook-posts-search) |
| [Create Data365 Instagram Profile Feed Posts Job](actions/create-data365-instagram-profile-feed-posts-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/data365-instagram-profile-feed-posts) |
| [Create Data365 Instagram Profile Search Job](actions/create-data365-instagram-profile-search-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/data365-instagram-profile-search) |
| [Create Data365 TikTok Keywords Job](actions/create-data365-tik-tok-keywords-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/data365-tiktok-keywords) |
| [Create Data365 X Keywords Job](actions/create-data365-x-keywords-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/data365-x-keywords) |
| [Create Job](actions/create-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/creating-jobs-portal-api) |
| [Create Opoint News Job](actions/create-opoint-news-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/opoint-news) |
| [Create Searchable Storage Aggregate Job](actions/create-searchable-storage-aggregate-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/searchable-storage-ingress) |
| [Create Searchable Storage Combined Search And Aggregate Job](actions/create-searchable-storage-combined-search-and-aggregate-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/searchable-storage-ingress) |
| [Create Searchable Storage Search Job](actions/create-searchable-storage-search-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/searchable-storage-ingress) |
| [Create Socialgist Blogs Job](actions/create-socialgist-blogs-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/socialgist-blogs) |
| [Create Socialgist Boards Job](actions/create-socialgist-boards-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/socialgist-boards) |
| [Create Socialgist News Job](actions/create-socialgist-news-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/socialgist-news) |
| [Create Socialgist Reddit Job](actions/create-socialgist-reddit-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/socialgist-reddit) |
| [Create Socialgist TikTok Job](actions/create-socialgist-tik-tok-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/socialgist-tiktok) |
| [Create WebSightLine Augmented Instagram Job](actions/create-web-sight-line-augmented-instagram-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/websightline-augmented-instagram) |
| [Create WebSightLine Instagram Job](actions/create-web-sight-line-instagram-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/websightline-instagram) |
| [Create WebSightLine Threads Job](actions/create-web-sight-line-threads-job.md) | `POST /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/websightline-threads) |
| [List Jobs](actions/list-jobs.md) | `GET /api/pipelines/:pipelineId/components/:componentId/jobs` | [docs](https://docs.datastreamer.io/docs/listing-jobs) |
| [Search Jobs](actions/search-jobs.md) | `POST /api/pipelines/jobs/search` | [docs](https://docs.datastreamer.io/docs/searching-jobs) |
| [Search Work Items](actions/search-work-items.md) | `POST /api/pipelines/work-items/search` | [docs](https://docs.datastreamer.io/docs/searching-work-items) |
