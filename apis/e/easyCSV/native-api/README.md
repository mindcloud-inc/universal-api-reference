# EasyCSV: Native API Reference

A consolidated summary of EasyCSV's API configuration and 2 documented operations.

- **API base URL:** `https://www.easycsv.io`

## Authentication

### API Key

Use your EasyCSV API key from the Business Info page for sheet-import webhook actions. CSV generator webhooks may not require the API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.easycsv.io/docs)

## Endpoints (2 documented)

| Operation | Method & path |
| --- | --- |
| [Generate CSV File](actions/generate-csv-file.md) | `POST /generate_csv/:generatorId` |
| [Import CSV File From URL](actions/import-csv-file-from-url.md) | `POST https://www.easycsv.io/:workspaceSlug/sheets/webhook/:webhookId` |
