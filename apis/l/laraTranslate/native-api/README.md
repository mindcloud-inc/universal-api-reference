# Lara Translate: Native API Reference

A consolidated summary of Lara Translate's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://developers.laratranslate.com/docs/getting-started-with-mcp
- **API base URL:** `https://mcp-v2.laratranslate.com/v1`

## Authentication

### Access key

Use a Lara Translate access key ID and secret to call the hosted MCP endpoint.

### Credentials

- **API Key:** `apiKey` · required
- **Access key ID:** `accessKeyId` · required · Your Lara Translate access key ID. Lara sends this value in the x-lara-access-key-id header.

Send these headers with each API request:

```http
x-lara-access-key-id: <accessKeyId>
x-lara-access-key-secret: <apiKey>
```

[Official authentication documentation](https://support.laratranslate.com/en/api-key-for-laras-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json, text/event-stream` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add translation unit to memory](actions/add-translation-unit-to-memory.md) | `POST /` | [docs](https://developers.laratranslate.com/docs/manage-translation-memories) |
| [Check memory import status](actions/check-memory-import-status.md) | `POST /` | [docs](https://developers.laratranslate.com/docs/manage-translation-memories) |
| [Create translation memory](actions/create-translation-memory.md) | `POST /` | [docs](https://developers.laratranslate.com/docs/manage-translation-memories) |
| [Delete translation memory](actions/delete-translation-memory.md) | `POST /` | [docs](https://developers.laratranslate.com/docs/manage-translation-memories) |
| [Delete translation unit from memory](actions/delete-translation-unit-from-memory.md) | `POST /` | [docs](https://developers.laratranslate.com/docs/manage-translation-memories) |
| [Detect language](actions/detect-language.md) | `POST /` | [docs](https://developers.laratranslate.com/docs/getting-started-with-mcp) |
| [Import TMX into memory](actions/import-tmx-into-memory.md) | `POST /` | [docs](https://developers.laratranslate.com/docs/manage-translation-memories) |
| [List supported languages](actions/list-supported-languages.md) | `POST /` | [docs](https://developers.laratranslate.com/docs/supported-languages) |
| [List translation memories](actions/list-translation-memories.md) | `POST /` | [docs](https://developers.laratranslate.com/docs/manage-translation-memories) |
| [Rename translation memory](actions/rename-translation-memory.md) | `POST /` | [docs](https://developers.laratranslate.com/docs/manage-translation-memories) |
| [Translate text](actions/translate-text.md) | `POST /` | [docs](https://developers.laratranslate.com/docs/translate-text) |
