# Daytona: Native API Reference

A consolidated summary of Daytona's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://www.daytona.io/docs/tools/api/
- **OpenAPI specification:** https://www.daytona.io/docs/openapi.json
- **API base URL:** `https://app.daytona.io/api`

## Authentication

### API Key

Use a Daytona API key as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.daytona.io/docs/)

## API conventions

Responses from this API use JSON. The total page count is read from `totalPages`. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Sandbox](actions/archive-sandbox.md) | `POST /sandbox/[:sandboxIdOrName]/archive` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Create Sandbox](actions/create-sandbox.md) | `POST /sandbox` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Create Sandbox Backup](actions/create-sandbox-backup.md) | `POST /sandbox/[:sandboxIdOrName]/backup` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Create Sandbox Snapshot](actions/create-sandbox-snapshot.md) | `POST /sandbox/[:sandboxIdOrName]/snapshot` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Create Sandbox SSH Access](actions/create-sandbox-ssh-access.md) | `POST /sandbox/[:sandboxIdOrName]/ssh-access` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Create Snapshot](actions/create-snapshot.md) | `POST /snapshots` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Create Volume](actions/create-volume.md) | `POST /volumes` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Delete Sandbox](actions/delete-sandbox.md) | `DELETE /sandbox/[:sandboxIdOrName]` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Delete Volume](actions/delete-volume.md) | `DELETE /volumes/[:volumeId]` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Get Current API Key](actions/get-current-api-key.md) | `GET /api-keys/current` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Get Port Preview URL](actions/get-port-preview-url.md) | `GET /sandbox/[:sandboxIdOrName]/ports/[:port]/preview-url` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Get Sandbox](actions/get-sandbox.md) | `GET /sandbox/[:sandboxIdOrName]` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Get Sandbox Build Logs URL](actions/get-sandbox-build-logs-url.md) | `GET /sandbox/[:sandboxIdOrName]/build-logs-url` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Get Sandbox Metrics](actions/get-sandbox-metrics.md) | `GET /sandbox/[:sandboxId]/telemetry/metrics` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Get Sandbox Region Quota](actions/get-sandbox-region-quota.md) | `GET /sandbox/[:sandboxId]/region-quota` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Get Sandbox Toolbox Proxy URL](actions/get-sandbox-toolbox-proxy-url.md) | `GET /sandbox/[:sandboxId]/toolbox-proxy-url` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Get Signed Port Preview URL](actions/get-signed-port-preview-url.md) | `GET /sandbox/[:sandboxIdOrName]/ports/[:port]/signed-preview-url` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Get Snapshot](actions/get-snapshot.md) | `GET /snapshots/[:id]` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Get Snapshot Build Logs URL](actions/get-snapshot-build-logs-url.md) | `GET /snapshots/[:id]/build-logs-url` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Get Volume](actions/get-volume.md) | `GET /volumes/[:volumeId]` | [docs](https://www.daytona.io/docs/tools/api/) |
| [List Available Regions](actions/list-available-regions.md) | `GET /regions` | [docs](https://www.daytona.io/docs/tools/api/) |
| [List Sandboxes Paginated](actions/list-sandboxes-paginated.md) | `GET /sandbox/paginated` | [docs](https://www.daytona.io/docs/tools/api/) |
| [List Shared Regions](actions/list-shared-regions.md) | `GET /shared-regions` | [docs](https://www.daytona.io/docs/tools/api/) |
| [List Snapshots](actions/list-snapshots.md) | `GET /snapshots` | [docs](https://www.daytona.io/docs/tools/api/) |
| [List Volumes](actions/list-volumes.md) | `GET /volumes` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Recover Sandbox](actions/recover-sandbox.md) | `POST /sandbox/[:sandboxIdOrName]/recover` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Replace Sandbox Labels](actions/replace-sandbox-labels.md) | `PUT /sandbox/[:sandboxIdOrName]/labels` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Revoke Sandbox SSH Access](actions/revoke-sandbox-ssh-access.md) | `DELETE /sandbox/[:sandboxIdOrName]/ssh-access` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Set Sandbox Autostop Interval](actions/set-sandbox-autostop-interval.md) | `POST /sandbox/[:sandboxIdOrName]/autostop/[:interval]` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Start Sandbox](actions/start-sandbox.md) | `POST /sandbox/[:sandboxIdOrName]/start` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Stop Sandbox](actions/stop-sandbox.md) | `POST /sandbox/[:sandboxIdOrName]/stop` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Update Sandbox Public Status](actions/update-sandbox-public-status.md) | `POST /sandbox/[:sandboxIdOrName]/public/[:isPublic]` | [docs](https://www.daytona.io/docs/tools/api/) |
| [Validate Sandbox SSH Access](actions/validate-sandbox-ssh-access.md) | `GET /sandbox/ssh-access/validate` | [docs](https://www.daytona.io/docs/tools/api/) |
