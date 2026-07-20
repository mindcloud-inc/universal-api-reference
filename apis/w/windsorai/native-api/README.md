# Windsor.ai: Native API Reference

A consolidated summary of Windsor.ai's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://windsor.ai/api-documentation/
- **API base URL:** `https://onboard.windsor.ai`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://windsor.ai/api-documentation/)

## API conventions

Responses from this API use JSON.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compare Multiple Platforms](actions/compare-multiple-platforms.md) | `GET https://connectors.windsor.ai/all` | [docs](https://windsor.ai/api-documentation/#tab-content42) |
| [Generate Authorization Link For A Single Data Source](actions/generate-authorization-link-for-a-single-data-source.md) | `GET /api/team/generate-co-user-url/` | [docs](https://windsor.ai/api-documentation/#tab-content28) |
| [Generate Authorization Link For Any Data Source](actions/generate-authorization-link-for-any-data-source.md) | `GET /api/team/generate-co-user-url` | [docs](https://windsor.ai/api-documentation/#tab-content29) |
| [Get Connector Data](actions/get-connector-data.md) | `GET https://connectors.windsor.ai/:connector` | [docs](https://windsor.ai/api-documentation/#tab-content6) |
| [List Accounts For All Data Sources](actions/list-accounts-for-all-data-sources.md) | `GET /api/common/ds-accounts` | [docs](https://windsor.ai/api-documentation/#tab-content36) |
| [List Co-User Linked Accounts](actions/list-co-user-linked-accounts.md) | `GET /api/team/co-user-linked-accounts/` | [docs](https://windsor.ai/api-documentation/#tab-content30) |
| [List Connectors](actions/list-connectors.md) | `GET https://connectors.windsor.ai/list_connectors` | [docs](https://windsor.ai/api-documentation/#tab-content17) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /api/custom-fields` | [docs](https://windsor.ai/api-documentation/#tab-content39) |
