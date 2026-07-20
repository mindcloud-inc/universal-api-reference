# Mapsly: Native API Reference

A consolidated summary of Mapsly's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://developer.mapsly.com/docs/api/ZG9jOjc1MTcyMDI-introduction-to-mapsly-api
- **API base URL:** `https://api.mapsly.com/v1`

## Authentication

### API Key

Authenticate Mapsly API requests with an API key sent as the apikey query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.mapsly.com/docs/api/ZG9jOjc1MTcyMDI-introduction-to-mapsly-api)

## API conventions

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Record Using GET](actions/delete-record-using-get.md) | `GET /deleterecord` | [docs](https://developer.mapsly.com/docs/api/reference/FORM-API.v1.yaml/paths/~1deleterecord/get) |
| [Delete Record Using POST](actions/delete-record-using-post.md) | `POST /deleterecord` | [docs](https://developer.mapsly.com/docs/api/reference/FORM-API.v1.yaml/paths/~1deleterecord/post) |
| [Delete Records](actions/delete-records.md) | `DELETE /record` | [docs](https://developer.mapsly.com/docs/api/reference/REST-API.v1.yaml/paths/~1record/delete) |
| [Upsert Record Using GET](actions/upsert-record-using-get.md) | `GET /updaterecord` | [docs](https://developer.mapsly.com/docs/api/reference/FORM-API.v1.yaml/paths/~1updaterecord/get) |
| [Upsert Record Using POST](actions/upsert-record-using-post.md) | `POST /updaterecord` | [docs](https://developer.mapsly.com/docs/api/reference/FORM-API.v1.yaml/paths/~1updaterecord/post) |
| [Upsert Records](actions/upsert-records.md) | `POST /record` | [docs](https://developer.mapsly.com/docs/api/reference/REST-API.v1.yaml/paths/~1record/post) |
