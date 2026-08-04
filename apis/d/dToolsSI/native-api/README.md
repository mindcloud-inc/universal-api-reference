# D-Tools SI: Native API Reference

A consolidated summary of D-Tools SI's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://api.d-tools.com/si/doc
- **API base URL:** `https://api.d-tools.com/SI/`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-DTSI-ApiKey: <apiKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Projects](actions/archive-projects.md) | `POST https://api.d-tools.com/SI/Publish/Projects/ArchiveProjects` | [docs](https://api.d-tools.com/SI/doc/Api/POST-Publish-Projects) |
| [Get Partial Project by Id](actions/get-partial-project.md) | `GET https://api.d-tools.com/SI/SubscribePartialProjects/Projects` | [docs](https://api.d-tools.com/SI/doc/Api/POST-Publish-Projects) |
| [Get Project by Id](actions/get-project.md) | `GET https://api.d-tools.com/SI/Subscribe/Projects` | [docs](https://api.d-tools.com/SI/doc/Api/POST-Publish-Projects) |
| [List Client Info](actions/list-client-info.md) | `GET Subscribe/Clients?includeImported={includeImported}&searchText={searchText}&includeDeleted={includeDeleted}&pageNumber={pageNumber}&pageSize={pageSize}` |  |
| [List Subscribed Projects](actions/list-subscribed-projects.md) | `GET Subscribe/Projects` |  |
| [Publish Projects](actions/publish-projects.md) | `POST https://api.d-tools.com/SI/Publish/Projects` | [docs](https://api.d-tools.com/SI/doc/Api/POST-Publish-Projects) |
| [Update Project](actions/update-project.md) | `POST https://api.d-tools.com/SI/Publish/Projects/Update` | [docs](https://api.d-tools.com/SI/doc/Api/POST-Publish-Projects) |
