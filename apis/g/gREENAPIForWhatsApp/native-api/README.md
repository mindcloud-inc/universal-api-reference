# GREEN-API for WhatsApp: Native API Reference

A consolidated summary of GREEN-API for WhatsApp's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://green-api.com/en/docs/api/
- **API base URL:** `{apiUrl}/waInstance{idInstance}/`

## Authentication

### Tenant Credentials

Provide your GREEN-API instance credentials from the GREEN-API console.

### Credentials

- **API URL:** `apiUrl` · required · API host from the GREEN-API console.
- **Media URL:** `mediaUrl` · required · Media host from the GREEN-API console.
- **Instance ID:** `idInstance` · required · Instance identifier from the GREEN-API console.
- **API Token:** `apiTokenInstance` · required · API token for the instance from the GREEN-API console.

[Official authentication documentation](https://green-api.com/en/docs/before-start/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Instance State](actions/get-instance-state.md) | `GET getStateInstance/:apiTokenInstance` | [docs](https://green-api.com/en/docs/api/account/GetStateInstance/) |
