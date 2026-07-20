# Leverly: Native API Reference

A consolidated summary of Leverly's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://leverly.com/kb-categories/integration-instructions/
- **API base URL:** `https://app.leverly.com/main`

## Authentication

### Account ID

Use your Leverly AccountID for direct HTTP posting and stop-call requests.

### Credentials

- **Account ID:** `accountId` · required · Your unique Leverly AccountID used in direct HTTP requests.

[Official authentication documentation](https://leverly.com/kb/http-posting/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Call](actions/create-call.md) | `POST /ingestor/process` | [docs](https://leverly.com/kb/http-posting/) |
| [Salesforce Stop Call](actions/salesforce-stop-call.md) | `POST /salesforce/unpark` | [docs](https://leverly.com/kb/salesforce-stop-calls/) |
| [Stop Call](actions/stop-call.md) | `POST /inquiry/unpark` | [docs](https://leverly.com/kb/http-stop-calls/) |
