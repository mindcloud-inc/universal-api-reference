# What3Words: Native API Reference

A consolidated summary of What3Words's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://developer.what3words.com/public-api/docs
- **OpenAPI specification:** https://openapi.what3words.com/openapi/openapi.json
- **API base URL:** `https://api.what3words.com/v3`

## Authentication

### API Key

what3words accepts API keys using the key query parameter or the X-Api-Key request header. This app sends the stored MindCloud API key as X-Api-Key and removes the default bearer Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://developer.what3words.com/public-api/docs)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Coordinates to what3words Address](actions/convert-coordinates-to-what3words-address.md) | `GET /convert-to-3wa` | [docs](https://developer.what3words.com/public-api/docs#convert-to-3-word-address) |
| [Convert what3words Address to Coordinates](actions/convert-what3words-address-to-coordinates.md) | `GET /convert-to-coordinates` | [docs](https://developer.what3words.com/public-api/docs#convert-to-coordinates) |
| [Get what3words Grid Section](actions/get-what3words-grid-section.md) | `GET /grid-section` | [docs](https://developer.what3words.com/public-api/docs#grid-section) |
| [List Available what3words Languages](actions/list-available-what3words-languages.md) | `GET /available-languages` | [docs](https://developer.what3words.com/public-api/docs#available-languages) |
| [Suggest what3words Addresses](actions/suggest-what3words-addresses.md) | `GET /autosuggest` | [docs](https://developer.what3words.com/public-api/docs#autosuggest) |
