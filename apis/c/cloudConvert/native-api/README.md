# CloudConvert: Native API Reference

A consolidated summary of CloudConvert's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://cloudconvert.com/docs/getting-started/introduction
- **API base URL:** `https://api.cloudconvert.com/v2`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://cloudconvert.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://cloudconvert.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `user.read user.write task.read task.write webhook.read webhook.write`.

[Official authentication documentation](https://cloudconvert.com/api/v2#oauth-2)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Task](actions/cancel-task.md) | `POST /tasks/:id/cancel` | [docs](https://cloudconvert.com/docs/api-reference/tasks) |
| [Create Archive Task](actions/create-archive-task.md) | `POST /archive` | [docs](https://cloudconvert.com/docs/operations/create-archives) |
| [Create Convert Task](actions/create-convert-task.md) | `POST /convert` | [docs](https://cloudconvert.com/docs/operations/convert-files) |
| [Create Export URL Task](actions/create-export-url-task.md) | `POST /export/url` | [docs](https://cloudconvert.com/docs/import-export/export-files) |
| [Create Import URL Task](actions/create-import-url-task.md) | `POST /import/url` | [docs](https://cloudconvert.com/docs/import-export/import-files) |
| [Create Job](actions/create-job.md) | `POST /jobs` | [docs](https://cloudconvert.com/docs/api-reference/jobs) |
| [Create Merge Task](actions/create-merge-task.md) | `POST /merge` | [docs](https://cloudconvert.com/docs/operations/merge-files) |
| [Create Metadata Task](actions/create-metadata-task.md) | `POST /metadata` | [docs](https://cloudconvert.com/docs/operations/file-metadata) |
| [Create Upload Task](actions/create-upload-task.md) | `POST /import/upload` | [docs](https://cloudconvert.com/docs/import-export/import-files) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://cloudconvert.com/docs/api-reference/webhooks) |
| [Delete Job](actions/delete-job.md) | `DELETE /jobs/:id` | [docs](https://cloudconvert.com/docs/api-reference/jobs) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:id` | [docs](https://cloudconvert.com/docs/api-reference/tasks) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://cloudconvert.com/docs/api-reference/webhooks) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://cloudconvert.com/docs/api-reference/users) |
| [Get Job](actions/get-job.md) | `GET /jobs/:id` | [docs](https://cloudconvert.com/docs/api-reference/jobs) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://cloudconvert.com/docs/api-reference/tasks) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://cloudconvert.com/docs/api-reference/jobs) |
| [List Possible Operations](actions/list-possible-operations.md) | `GET /operations` | [docs](https://cloudconvert.com/docs/api-reference/operations) |
| [List Supported Formats](actions/list-supported-formats.md) | `GET /convert/formats` | [docs](https://cloudconvert.com/docs/api-reference/operations) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://cloudconvert.com/docs/api-reference/tasks) |
| [List Webhooks](actions/list-webhooks.md) | `GET /users/me/webhooks` | [docs](https://cloudconvert.com/docs/api-reference/webhooks) |
| [Retry Task](actions/retry-task.md) | `POST /tasks/:id/retry` | [docs](https://cloudconvert.com/docs/api-reference/tasks) |
| [Wait for Job](actions/wait-for-job.md) | `GET https://sync.api.cloudconvert.com/v2/jobs/:id/wait` | [docs](https://cloudconvert.com/docs/api-reference/jobs) |
| [Wait for Task](actions/wait-for-task.md) | `GET https://sync.api.cloudconvert.com/v2/tasks/:id/wait` | [docs](https://cloudconvert.com/docs/api-reference/tasks) |
