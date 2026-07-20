# Bump.sh: Native API Reference

A consolidated summary of Bump.sh's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://developers.bump.sh/
- **OpenAPI specification:** https://developers.bump.sh/source.json
- **API base URL:** `https://bump.sh/api/v1`

## Authentication

### API Key

Use a Bump.sh API token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.bump.sh/authentication.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Branch](actions/create-branch.md) | `POST docs/:doc_id_or_slug/branches` | [docs](https://developers.bump.sh/source.json#/paths/~1docs~1{doc_id_or_slug}~1branches/post) |
| [Create Diff](actions/create-diff.md) | `POST diffs` | [docs](https://developers.bump.sh/source.json#/paths/~1diffs/post) |
| [Create Preview](actions/create-preview.md) | `POST previews` | [docs](https://developers.bump.sh/source.json#/paths/~1previews/post) |
| [Create Version](actions/create-version.md) | `POST versions` | [docs](https://developers.bump.sh/operation/operation-post-versions) |
| [Delete Branch](actions/delete-branch.md) | `DELETE docs/:doc_id_or_slug/branches/:slug` | [docs](https://developers.bump.sh/source.json#/paths/~1docs~1{doc_id_or_slug}~1branches~1{slug}/delete) |
| [Deploy MCP Server Document](actions/deploy-mcp-server-document.md) | `POST mcp_servers/:mcp_server_id_or_slug/deploy` | [docs](https://developers.bump.sh/source.json#/paths/~1mcp_servers~1{mcp_server_id_or_slug}~1deploy/post) |
| [Get Diff](actions/get-diff.md) | `GET diffs/:id` | [docs](https://developers.bump.sh/source.json#/paths/~1diffs~1{id}/get) |
| [Get Hub](actions/get-hub.md) | `GET hubs/:hub_id_or_slug` | [docs](https://developers.bump.sh/source.json#/paths/~1hubs~1{hub_id_or_slug}/get) |
| [Get Version](actions/get-version.md) | `GET versions/:version_id` | [docs](https://developers.bump.sh/source.json#/paths/~1versions~1{version_id}/get) |
| [List Branches](actions/list-branches.md) | `GET docs/:doc_id_or_slug/branches` | [docs](https://developers.bump.sh/source.json#/paths/~1docs~1{doc_id_or_slug}~1branches/get) |
| [List Hubs](actions/list-hubs.md) | `GET hubs` | [docs](https://developers.bump.sh/operation/operation-listhubs) |
| [Ping](actions/ping.md) | `GET ping` | [docs](https://developers.bump.sh/source.json#/paths/~1ping/get) |
| [Set Default Branch](actions/set-default-branch.md) | `PATCH docs/:doc_id_or_slug/branches/:slug/set_default` | [docs](https://developers.bump.sh/source.json#/paths/~1docs~1{doc_id_or_slug}~1branches~1{slug}~1set_default/patch) |
| [Update Preview](actions/update-preview.md) | `PUT previews/:preview_id` | [docs](https://developers.bump.sh/source.json#/paths/~1previews~1{preview_id}/put) |
| [Validate Definition](actions/validate-definition.md) | `POST validations` | [docs](https://developers.bump.sh/source.json#/paths/~1validations/post) |
