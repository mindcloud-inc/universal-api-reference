# E2B: Native API Reference

A consolidated summary of E2B's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://e2b.dev/docs
- **API base URL:** `https://api.e2b.app`

## Authentication

### API Key

Use an E2B API key. E2B expects the key in the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://e2b.dev/docs/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; minimum 1). Use `nextToken` in the query string as the pagination cursor; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Tags](actions/assign-tags.md) | `POST /templates/tags` | [docs](https://e2b.dev/docs/api-reference/tags/assign-tags) |
| [Connect To Sandbox](actions/connect-to-sandbox.md) | `POST /sandboxes/{sandboxID}/connect` | [docs](https://e2b.dev/docs/api-reference/sandboxes/connect-to-sandbox) |
| [Create Sandbox](actions/create-sandbox.md) | `POST /sandboxes` | [docs](https://e2b.dev/docs/api-reference/sandboxes/create-sandbox) |
| [Create Sandbox Snapshot](actions/create-sandbox-snapshot.md) | `POST /sandboxes/{sandboxID}/snapshots` | [docs](https://e2b.dev/docs/api-reference/sandboxes/post-sandboxes-snapshots) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://e2b.dev/docs/api-reference/templates/create-template) |
| [Create Template V3](actions/create-template-v3.md) | `POST /v3/templates` | [docs](https://e2b.dev/docs/api-reference/templates/create-template-v3) |
| [Create Volume](actions/create-volume.md) | `POST /volumes` | [docs](https://e2b.dev/docs/api-reference/volumes/post-volumes) |
| [Delete Sandbox](actions/delete-sandbox.md) | `DELETE /sandboxes/{sandboxID}` | [docs](https://e2b.dev/docs/api-reference/sandboxes/delete-sandbox) |
| [Delete Tags](actions/delete-tags.md) | `DELETE /templates/tags` | [docs](https://e2b.dev/docs/api-reference/tags/delete-tags) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/{templateID}` | [docs](https://e2b.dev/docs/api-reference/templates/delete-template) |
| [Delete Volume](actions/delete-volume.md) | `DELETE /volumes/{volumeID}` | [docs](https://e2b.dev/docs/api-reference/volumes/delete-volumes) |
| [Get Build Logs](actions/get-build-logs.md) | `GET /templates/{templateID}/builds/{buildID}/logs` | [docs](https://e2b.dev/docs/api-reference/templates/get-build-logs) |
| [Get Build Status](actions/get-build-status.md) | `GET /templates/{templateID}/builds/{buildID}/status` | [docs](https://e2b.dev/docs/api-reference/templates/get-build-status) |
| [Get Build Upload Link](actions/get-build-upload-link.md) | `GET /templates/{templateID}/files/{hash}` | [docs](https://e2b.dev/docs/api-reference/templates/get-build-upload-link) |
| [Get Sandbox](actions/get-sandbox.md) | `GET /sandboxes/{sandboxID}` | [docs](https://e2b.dev/docs/api-reference/sandboxes/get-sandbox) |
| [Get Sandbox Logs V2](actions/get-sandbox-logs-v2.md) | `GET /v2/sandboxes/{sandboxID}/logs` | [docs](https://e2b.dev/docs/api-reference/sandboxes/get-sandbox-logs-v2) |
| [Get Sandbox Metrics](actions/get-sandbox-metrics.md) | `GET /sandboxes/{sandboxID}/metrics` | [docs](https://e2b.dev/docs/api-reference/sandboxes/get-sandbox-metrics) |
| [Get Template](actions/get-template.md) | `GET /templates/{templateID}` | [docs](https://e2b.dev/docs/api-reference/templates/get-template) |
| [Get Template By Alias](actions/get-template-by-alias.md) | `GET /templates/aliases/{alias}` | [docs](https://e2b.dev/docs/api-reference/templates/get-template-by-alias) |
| [Get Volume](actions/get-volume.md) | `GET /volumes/{volumeID}` | [docs](https://e2b.dev/docs/api-reference/volumes/get-volumes-1) |
| [List Sandbox Metrics](actions/list-sandbox-metrics.md) | `GET /sandboxes/metrics` | [docs](https://e2b.dev/docs/api-reference/sandboxes/list-sandbox-metrics) |
| [List Sandboxes](actions/list-sandboxes.md) | `GET /sandboxes` | [docs](https://e2b.dev/docs/api-reference/sandboxes/list-sandboxes) |
| [List Sandboxes V2](actions/list-sandboxes-v2.md) | `GET /v2/sandboxes` | [docs](https://e2b.dev/docs/api-reference/sandboxes/list-sandboxes-v2) |
| [List Snapshots](actions/list-snapshots.md) | `GET /snapshots` | [docs](https://e2b.dev/docs/api-reference/sandboxes/get-snapshots) |
| [List Template Tags](actions/list-template-tags.md) | `GET /templates/{templateID}/tags` | [docs](https://e2b.dev/docs/api-reference/tags/list-template-tags) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://e2b.dev/docs/api-reference/templates/list-templates) |
| [List Volumes](actions/list-volumes.md) | `GET /volumes` | [docs](https://e2b.dev/docs/api-reference/volumes/get-volumes) |
| [Pause Sandbox](actions/pause-sandbox.md) | `POST /sandboxes/{sandboxID}/pause` | [docs](https://e2b.dev/docs/api-reference/sandboxes/pause-sandbox) |
| [Rebuild Template](actions/rebuild-template.md) | `POST /templates/{templateID}` | [docs](https://e2b.dev/docs/api-reference/templates/rebuild-template) |
| [Refresh Sandbox](actions/refresh-sandbox.md) | `POST /sandboxes/{sandboxID}/refreshes` | [docs](https://e2b.dev/docs/api-reference/sandboxes/refresh-sandbox) |
| [Resume Sandbox](actions/resume-sandbox.md) | `POST /sandboxes/{sandboxID}/resume` | [docs](https://e2b.dev/docs/api-reference/sandboxes/resume-sandbox) |
| [Set Sandbox Timeout](actions/set-sandbox-timeout.md) | `POST /sandboxes/{sandboxID}/timeout` | [docs](https://e2b.dev/docs/api-reference/sandboxes/set-sandbox-timeout) |
| [Start Build](actions/start-build.md) | `POST /templates/{templateID}/builds/{buildID}` | [docs](https://e2b.dev/docs/api-reference/templates/start-build) |
| [Start Build V2](actions/start-build-v2.md) | `POST /v2/templates/{templateID}/builds/{buildID}` | [docs](https://e2b.dev/docs/api-reference/templates/start-build-v2) |
| [Update Sandbox Network](actions/update-sandbox-network.md) | `PUT /sandboxes/{sandboxID}/network` | [docs](https://e2b.dev/docs/api-reference/sandboxes/put-sandboxes-network) |
| [Update Template](actions/update-template.md) | `PATCH /templates/{templateID}` | [docs](https://e2b.dev/docs/api-reference/templates/update-template) |
| [Update Template V2](actions/update-template-v2.md) | `PATCH /v2/templates/{templateID}` | [docs](https://e2b.dev/docs/api-reference/templates/update-template-v2) |
