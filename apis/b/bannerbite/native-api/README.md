# Bannerbite: Native API Reference

A consolidated summary of Bannerbite's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://developer.bannerbite.com/
- **API base URL:** `https://api.bannerbite.com`

## Authentication

### Bannerbite API Key

Use a Bannerbite API key from My Account -> API Settings to authenticate REST requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.bannerbite.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Image Or Video](actions/generate-image-or-video.md) | `POST /api/render` | [docs](https://developer.bannerbite.com/) |
| [Get Bite](actions/get-bite.md) | `GET /api/bites/:id` | [docs](https://developer.bannerbite.com/) |
| [Get Project](actions/get-project.md) | `GET /api/projects/:id` | [docs](https://developer.bannerbite.com/) |
| [Get Scene Data](actions/get-scene-data.md) | `GET /api/sceneData/:id` | [docs](https://developer.bannerbite.com/) |
| [List Bites](actions/list-bites.md) | `GET /api/bites` | [docs](https://developer.bannerbite.com/) |
| [List Projects](actions/list-projects.md) | `GET /api/projects` | [docs](https://developer.bannerbite.com/) |
| [Render From Make](actions/render-from-make.md) | `POST /api/integromat/render` | [docs](https://developer.bannerbite.com/) |
