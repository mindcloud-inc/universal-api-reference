# Apiary: Native API Reference

A consolidated summary of Apiary's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://apiary.docs.apiary.io/
- **API base URL:** `https://api.apiary.io`

## Authentication

### API Token

Use one Apiary personal token. Some Apiary routes require `Authentication: Token <token>` while others require `Authorization: Bearer <token>`, so native apiKey auth does not match the provider contract.

### Credentials

- **Token:** `token` · optional · Apiary personal token from https://login.apiary.io/tokens. The same token is reused across the bearer and token header variants required by Apiary.

Send these headers with each API request:

```http
Authorization: Bearer <token>
```

[Official authentication documentation](https://help.apiary.io/tools/apiary-cli/)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Fetch Blueprint](actions/fetch-blueprint.md) | `GET /blueprint/get/{{apiName}}` | [docs](https://apiary.docs.apiary.io/reference/fetch-blueprint) |
| [Get API Blueprint Snapshot](actions/get-api-blueprint-snapshot.md) | `GET https://jsapi.apiary.io/apis/{{apiName}}/blueprint` |  |
| [Get API Documentation Snapshot](actions/get-api-documentation-snapshot.md) | `GET https://jsapi.apiary.io/apis/{{apiName}}/documentation` |  |
| [Get API Summary](actions/get-api-summary.md) | `GET https://jsapi.apiary.io/apis/{{apiName}}` |  |
| [List APIs](actions/list-ap-is.md) | `GET /me/apis` | [docs](https://apiary.docs.apiary.io/reference/api-list) |
| [Publish Blueprint](actions/publish-blueprint.md) | `POST /blueprint/publish/{{apiName}}` | [docs](https://apiary.docs.apiary.io/reference/publish-blueprint) |
