# WorkAdventure: Native API Reference

A consolidated summary of WorkAdventure's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.workadventu.re/developer/
- **OpenAPI specification:** https://admin.workadventu.re/docs/api-docs.json
- **API base URL:** `https://admin.workadventu.re`

## Authentication

### API token

Provide a WorkAdventure developer token. The token is sent verbatim in the Authorization header with no Bearer prefix.

### Credentials

- **API token:** `apiToken` · required · Developer token generated in WorkAdventure Settings > Developers > Tokens. MindCloud sends this value verbatim in the Authorization header.

Send these headers with each API request:

```http
Authorization: <apiToken>
Authorization: Bearer <apiToken>
Authorization: Bearer <jwt>
```

[Official authentication documentation](https://docs.workadventu.re/developer/inbound-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy map file](actions/copy-map-file.md) | `POST https://mindcloud-34294.map-storage.workadventu.re/copy` | [docs](https://github.com/workadventure/workadventure/tree/develop/map-storage) |
| [Create member](actions/create-member.md) | `POST /api/v1/worlds/:worldSlug/members` | [docs](https://docs.workadventu.re/developer/inbound-api) |
| [Delete map file](actions/delete-map-file.md) | `DELETE https://mindcloud-34294.map-storage.workadventu.re/:filePath` | [docs](https://github.com/workadventure/workadventure/tree/develop/map-storage) |
| [Delete member](actions/delete-member.md) | `DELETE /api/v1/worlds/:worldSlug/members/:memberIdentifier` | [docs](https://docs.workadventu.re/developer/inbound-api) |
| [Download map archive](actions/download-map-archive.md) | `GET https://mindcloud-34294.map-storage.workadventu.re/download` | [docs](https://github.com/workadventure/workadventure/tree/develop/map-storage) |
| [Get file](actions/get-file.md) | `GET https://mindcloud-34294.map-storage.workadventu.re/:filePath` | [docs](https://docs.workadventu.re/developer/map-storage-api/) |
| [Get map storage index](actions/get-map-storage-index.md) | `GET https://mindcloud-34294.map-storage.workadventu.re/` | [docs](https://github.com/workadventure/workadventure/tree/develop/map-storage) |
| [Get member](actions/get-member.md) | `GET /api/v1/worlds/:worldSlug/members/:memberIdentifier` | [docs](https://docs.workadventu.re/developer/inbound-api) |
| [Get private file](actions/get-private-file.md) | `GET https://mindcloud-34294.map-storage.workadventu.re/private/files/:filePath` | [docs](https://docs.workadventu.re/developer/map-storage-api/) |
| [Get WAM file](actions/get-wam-file.md) | `GET https://mindcloud-34294.map-storage.workadventu.re/:wamPath` | [docs](https://github.com/workadventure/workadventure/tree/develop/map-storage) |
| [Get world details](actions/get-world-details.md) | `GET /api/v1/worlds/:worldSlug` | [docs](https://docs.workadventu.re/developer/inbound-api) |
| [List maps](actions/list-maps.md) | `GET https://mindcloud-34294.map-storage.workadventu.re/maps` | [docs](https://github.com/workadventure/workadventure/tree/develop/map-storage) |
| [List members](actions/list-members.md) | `GET /api/v1/worlds/:worldSlug/members` | [docs](https://docs.workadventu.re/developer/inbound-api) |
| [Move map file](actions/move-map-file.md) | `POST https://mindcloud-34294.map-storage.workadventu.re/move` | [docs](https://github.com/workadventure/workadventure/tree/develop/map-storage) |
| [Ping map storage](actions/ping-map-storage.md) | `GET https://mindcloud-34294.map-storage.workadventu.re/ping` | [docs](https://github.com/workadventure/workadventure/tree/develop/map-storage) |
| [Update member](actions/update-member.md) | `PATCH /api/v1/worlds/:worldSlug/members/:memberIdentifier` | [docs](https://docs.workadventu.re/developer/inbound-api) |
| [Upload file](actions/upload-file.md) | `PUT https://mindcloud-34294.map-storage.workadventu.re/:filePath` | [docs](https://docs.workadventu.re/developer/map-storage-api/) |
| [Upload map archive](actions/upload-map-archive.md) | `POST https://mindcloud-34294.map-storage.workadventu.re/upload` | [docs](https://docs.workadventu.re/developer/map-storage-api/) |
| [Upload WAM file](actions/upload-wam-file.md) | `PUT https://mindcloud-34294.map-storage.workadventu.re/:wamPath` | [docs](https://github.com/workadventure/workadventure/tree/develop/map-storage) |
| [Validate map](actions/validate-map.md) | `GET https://mindcloud-34294.map-storage.workadventu.re/validate` | [docs](https://docs.workadventu.re/developer/map-storage) |
