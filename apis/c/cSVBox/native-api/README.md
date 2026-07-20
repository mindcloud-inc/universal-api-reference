# CSVBox: Native API Reference

A consolidated summary of CSVBox's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://help.csvbox.io/advanced-installation
- **API base URL:** `https://api.csvbox.io/1.1`

## Authentication

### API Key

Use your CSVBox API key and Secret API Key from the CSVBox Accounts page.

### Credentials

- **API Key:** `apiKey` · required
- **Secret API Key:** `authSecret` · required · Secret API Key from the CSVBox Accounts page.

Send these headers with each API request:

```http
x-csvbox-api-key: <apiKey>
x-csvbox-secret-api-key: <authSecret>
```

[Official authentication documentation](https://help.csvbox.io/advanced-installation/auth-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Submit File From Public URL](actions/submit-file-from-public-url.md) | `POST /file` | [docs](https://help.csvbox.io/advanced-installation/rest-file-api) |
| [Upload File](actions/upload-file.md) | `POST /file` | [docs](https://help.csvbox.io/advanced-installation/rest-file-api) |
| [Verify Connection](actions/verify-connection.md) | `POST /auth` | [docs](https://help.csvbox.io/advanced-installation/auth-api) |
