# Convertio: Native API Reference

A consolidated summary of Convertio's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://developers.convertio.co/api/docs/
- **API base URL:** `https://api.convertio.co`

## Authentication

### API Key

Use your Convertio API key. Convertio expects the key in the JSON request body as `apikey`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.convertio.co/hc/en-us/articles/360006894493-How-to-obtain-an-API-key)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Conversion](actions/delete-conversion.md) | `DELETE /convert/:id` | [docs](https://developers.convertio.co/api/docs/) |
| [Get Conversion Status](actions/get-conversion-status.md) | `GET /convert/:id/status` | [docs](https://developers.convertio.co/api/docs/) |
| [Get Result File Content](actions/get-result-file-content.md) | `GET /convert/:id/dl/:type` | [docs](https://developers.convertio.co/api/docs/) |
| [List Conversions](actions/list-conversions.md) | `POST /convert/list` | [docs](https://developers.convertio.co/api/docs/) |
| [Start Conversion](actions/start-conversion.md) | `POST /convert` | [docs](https://developers.convertio.co/api/docs/) |
| [Upload Conversion File](actions/upload-conversion-file.md) | `PUT /convert/:id/:filename` | [docs](https://developers.convertio.co/api/docs/) |
