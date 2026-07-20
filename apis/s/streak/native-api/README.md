# Streak: Native API Reference

A consolidated summary of Streak's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://streak.readme.io/reference
- **API base URL:** `https://api.streak.com`

## Authentication

### Streak API Key

Use your Streak API key in both fields. Streak authenticates over Basic Auth with the API key as the username, and allows the same API key to be reused as the password for third-party software.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://streak.readme.io/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Box](actions/create-box.md) | `POST /api/v2/pipelines/:pipelineKey/boxes` | [docs](https://streak.readme.io/reference/create-a-box) |
| [Create Comment](actions/create-comment.md) | `POST /api/v2/boxes/:boxKey/comments` | [docs](https://streak.readme.io/reference/create-a-comment) |
| [Create Contact](actions/create-contact.md) | `POST /api/v2/teams/:teamKey/contacts/` | [docs](https://streak.readme.io/reference/create-a-contact) |
| [Create Task](actions/create-task.md) | `POST /api/v2/boxes/:boxKey/tasks` | [docs](https://streak.readme.io/reference/create-a-task) |
| [Get Box](actions/get-box.md) | `GET /api/v1/boxes/:boxKey` | [docs](https://streak.readme.io/reference/get-a-box) |
| [Get Box Timeline](actions/get-box-timeline.md) | `GET /api/v2/boxes/:boxKey/timeline` | [docs](https://streak.readme.io/reference/get-timeline-for-a-box) |
| [Get Contact](actions/get-contact.md) | `GET /api/v2/contacts/:contactKey` | [docs](https://streak.readme.io/reference/read-a-contact-1) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v1/users/me` | [docs](https://streak.readme.io/reference/get-current-user) |
| [Get multiple boxes](actions/get-multiple-boxes.md) | `POST /api/v1/pipelines/:pipelineKey/boxes/batch/` | [docs](https://streak.readme.io/reference/get-multiple-boxes) |
| [Get or Create Organization](actions/get-or-create-organization.md) | `POST /api/v2/teams/:teamKey/organizations` | [docs](https://streak.readme.io/reference/create-an-organization) |
| [Get Organization](actions/get-organization.md) | `GET /api/v2/organizations/:organizationKey` | [docs](https://streak.readme.io/reference/get-an-organization) |
| [Get Pipeline](actions/get-pipeline.md) | `GET /api/v1/pipelines/:pipelineKey` | [docs](https://streak.readme.io/reference/getting-a-specific-pipeline) |
| [List Box Comments](actions/list-box-comments.md) | `GET /api/v2/boxes/:boxKey/comments` | [docs](https://streak.readme.io/reference/get-all-comments) |
| [List Box Tasks](actions/list-box-tasks.md) | `GET /api/v2/boxes/:boxKey/tasks` | [docs](https://streak.readme.io/reference/read-tasks-on-a-box) |
| [List Box Threads](actions/list-box-threads.md) | `GET /api/v1/boxes/:boxKey/threads` | [docs](https://streak.readme.io/reference/get-threads-in-a-box) |
| [List Pipeline Boxes](actions/list-pipeline-boxes.md) | `GET /api/v1/pipelines/:pipelineKey/boxes` | [docs](https://streak.readme.io/reference/list-all-boxes-in-pipeline) |
| [List Pipeline Fields](actions/list-pipeline-fields.md) | `GET /api/v1/pipelines/:pipelineKey/fields` | [docs](https://streak.readme.io/reference/list-all-fields-in-a-pipeline) |
| [List Pipeline Stages](actions/list-pipeline-stages.md) | `GET /api/v1/pipelines/:pipelineKey/stages` | [docs](https://streak.readme.io/reference/list-all-stages-in-pipeline) |
| [List Pipelines](actions/list-pipelines.md) | `GET /api/v1/pipelines` | [docs](https://streak.readme.io/reference/list-all-pipelines) |
| [Search Boxes By Name](actions/search-boxes-by-name.md) | `GET /api/v1/search` | [docs](https://streak.readme.io/reference/searchng-for-boxes-by-name) |
| [Search Boxes, Contacts, and Organizations](actions/search-boxes-contacts-and-organizations.md) | `GET /api/v1/search` | [docs](https://streak.readme.io/reference/searching-for-boxes-contacts-and-organizations) |
| [Update Box](actions/update-box.md) | `POST /api/v1/boxes/:boxKey` | [docs](https://streak.readme.io/reference/edit-a-box) |
| [Update Contact](actions/update-contact.md) | `POST /api/v2/contacts/:contactKey` | [docs](https://streak.readme.io/reference/update-a-contact-1) |
| [Update Organization](actions/update-organization.md) | `POST /api/v2/organizations/:organizationKey` | [docs](https://streak.readme.io/reference/update-an-organization) |
| [Update Task](actions/update-task.md) | `POST /api/v2/tasks/:taskKey` | [docs](https://streak.readme.io/reference/update-a-task) |
