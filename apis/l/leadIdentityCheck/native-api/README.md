# Lead Identity Check: Native API Reference

A consolidated summary of Lead Identity Check's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://leadidentitycheck.com/documentation/
- **API base URL:** `https://leadidentitycheck-node.vercel.app`

## Authentication

### API Key + Filter Key

Use your Lead Identity Check tenant API key and filter key.

### Credentials

- **API Key:** `apiKey` · required · Your Lead Identity Check X-LIC-KEY value.
- **Filter Key:** `filterKey` · required · Your Lead Identity Check Filterkey value.

Send these headers with each API request:

```http
Filterkey: <filterKey>
X-LIC-KEY: <apiKey>
```

[Official authentication documentation](https://leadidentitycheck.com/documentation/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate Connection](actions/authenticate-connection.md) | `POST /zapier/authentication` | [docs](https://leadidentitycheck.com/documentation/) |
| [List Filter Categories](actions/list-filter-categories.md) | `POST /filters/categories` | [docs](https://leadidentitycheck.com/documentation/) |
| [Verify Lead](actions/verify-lead.md) | `POST /main/lic/v1` | [docs](https://leadidentitycheck.com/documentation/) |
