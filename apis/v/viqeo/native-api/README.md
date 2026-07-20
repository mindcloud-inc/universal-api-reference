# Viqeo: Native API Reference

A consolidated summary of Viqeo's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://support.viqeo.tv/en/articles/8962790-media-editor-api
- **API base URL:** `https://api.viqeo.tv`

## Authentication

### API Key

Use a Viqeo administrator token in the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.viqeo.tv/en/articles/8962790-media-editor-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate Project User](actions/authenticate-project-user.md) | `POST /media-platform/v1/project/:projectId/user/:email/authenticate` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_e0bfa8f879) |
| [Create Project](actions/create-project.md) | `PUT /media-platform/v1/project` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_fd2e63d987) |
| [Create Project User](actions/create-project-user.md) | `PUT /media-platform/v1/project/:projectId/user` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_e0bfa8f879) |
| [Create Story](actions/create-story.md) | `PUT /media-platform/v1/project/:projectId/story` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_ee34c919cc) |
| [Delete Project](actions/delete-project.md) | `DELETE /media-platform/v1/project/:projectId` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_fd2e63d987) |
| [Delete Project User](actions/delete-project-user.md) | `DELETE /media-platform/v1/project/:projectId/user/:email` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_e0bfa8f879) |
| [Delete Story](actions/delete-story.md) | `DELETE /media-platform/v1/project/:projectId/story/:storyId` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_ee34c919cc) |
| [Get Project](actions/get-project.md) | `GET /media-platform/v1/project/:projectId` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_fd2e63d987) |
| [Get Project User](actions/get-project-user.md) | `GET /media-platform/v1/project/:projectId/user/:email` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_e0bfa8f879) |
| [Get Story](actions/get-story.md) | `GET /media-platform/v1/project/:projectId/story/:storyId` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_ee34c919cc) |
| [List Project Users](actions/list-project-users.md) | `GET /media-platform/v1/project/:projectId/user` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_e0bfa8f879) |
| [List Projects](actions/list-projects.md) | `GET /media-platform/v1/project` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_fd2e63d987) |
| [List Stories](actions/list-stories.md) | `GET /media-platform/v1/project/:projectId/story` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_ee34c919cc) |
| [Update Project](actions/update-project.md) | `POST /media-platform/v1/project/:projectId` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_fd2e63d987) |
| [Update Story](actions/update-story.md) | `POST /media-platform/v1/project/:projectId/story/:storyId` | [docs](https://support.viqeo.tv/en/articles/8962790-media-editor-api#h_ee34c919cc) |
