# OpenCage: Native API Reference

A consolidated summary of OpenCage's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://opencagedata.com/api
- **OpenAPI specification:** https://opencagedata.com/openapi.yaml
- **API base URL:** `https://api.opencagedata.com/geocode/v1`

## Authentication

### API Key

OpenCage API key passed as the required `key` query parameter on every request.

### Credentials

- **API Key:** `apiKey` · required · OpenCage Geocoding API key from the Geocoding section of your OpenCage account dashboard.

[Official authentication documentation](https://opencagedata.com/api)

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100).

## Retry behavior

Retry responses with status codes `408,429,503`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Forward Geocode](actions/forward-geocode.md) | `GET /json` | [docs](https://opencagedata.com/api) |
| [Reverse Geocode](actions/reverse-geocode.md) | `GET /json` | [docs](https://opencagedata.com/api) |
