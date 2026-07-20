# Metance: Native API Reference

A consolidated summary of Metance's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://api.metance.com/index.html
- **OpenAPI specification:** https://api.metance.com/swagger/VaultOpenApiSpecification/swagger.json
- **API base URL:** `https://api.metance.com`

## Authentication

### Workspace Session Token

Use a Metance bearer session token together with workspace tenant context to access workspace data.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace ID:** `workspaceId` · required · Numeric Metance workspace identifier used for tenant-scoped API requests.
- **Subdomain:** `subdomain` · required · Workspace subdomain used by Metance tenant-scoped API requests.

Send these headers with each API request:

```http
subdomain: <subdomain>
X-Tenant-Id: <workspaceId>
```

[Official authentication documentation](https://api.metance.com/index.html)

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Content By ID](actions/get-content-by-id.md) | `GET /contents/{id}` | [docs](https://api.metance.com/index.html) |
| [Get Content By URL](actions/get-content-by-url.md) | `GET /contents/Url/{url}` | [docs](https://api.metance.com/index.html) |
| [Get Content Types](actions/get-content-types.md) | `GET /contentTypes` | [docs](https://api.metance.com/index.html) |
| [Get Current Company](actions/get-current-company.md) | `GET /master/currentcompany` | [docs](https://api.metance.com/index.html) |
| [Get Current Session](actions/get-current-session.md) | `GET /master/currentsession` | [docs](https://api.metance.com/index.html) |
| [Get Folders](actions/get-folders.md) | `GET /folders` | [docs](https://api.metance.com/index.html) |
| [Get Section Contents](actions/get-section-contents.md) | `GET /contents` | [docs](https://api.metance.com/index.html) |
| [Get Topics](actions/get-topics.md) | `GET /topics` | [docs](https://api.metance.com/index.html) |
| [List Files](actions/list-files.md) | `GET /file/list` | [docs](https://api.metance.com/index.html) |
