# Murf Dub: Native API Reference

A consolidated summary of Murf Dub's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://murf.ai/api/docs/capabilities/dubbing
- **API base URL:** `https://api.murf.ai`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://murf.ai/api/docs/capabilities/dubbing)

## Pagination

Use `limit` in the query string to set the page size. Use `next` in the query string as the pagination cursor.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Dubbing Job](actions/create-dubbing-job.md) | `POST /v1/murfdub/jobs/create` | [docs](https://murf.ai/api/docs/api-reference/dubbing/jobs/create) |
| [Create Dubbing Job With Project ID](actions/create-dubbing-job-with-project-id.md) | `POST /v1/murfdub/jobs/create-with-project-id` | [docs](https://murf.ai/api/docs/api-reference/dubbing/jobs/create-with-project-id) |
| [Create Dubbing Project](actions/create-dubbing-project.md) | `POST /v1/murfdub/projects/create` | [docs](https://murf.ai/api/docs/api-reference/dubbing/projects/create) |
| [Get Dubbing Job Status](actions/get-dubbing-job-status.md) | `GET /v1/murfdub/jobs/:job_id/status` | [docs](https://murf.ai/api/docs/api-reference/dubbing/jobs/get-status) |
| [List Destination Languages](actions/list-destination-languages.md) | `GET /v1/murfdub/list-destination-languages` | [docs](https://murf.ai/api/docs/api-reference/dubbing/languages/list-destination-languages) |
| [List Dubbing Projects](actions/list-dubbing-projects.md) | `GET /v1/murfdub/projects/list` | [docs](https://murf.ai/api/docs/api-reference/dubbing/projects/list) |
| [List Source Languages](actions/list-source-languages.md) | `GET /v1/murfdub/list-source-languages` | [docs](https://murf.ai/api/docs/api-reference/dubbing/languages/list-source-languages) |
| [Update Dubbing Project](actions/update-dubbing-project.md) | `PUT /v1/murfdub/projects/:project_id/update` | [docs](https://murf.ai/api/docs/api-reference/dubbing/projects/update) |
