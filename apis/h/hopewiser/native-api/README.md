# Hopewiser: Native API Reference

A consolidated summary of Hopewiser's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://www.hopewiser.com/developer-document/developer-documentation/
- **API base URL:** `https://cloud.hopewiser.com`

## Authentication

### Basic Auth

Use the Hopewiser API token username and token password with HTTP Basic Authentication.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.hopewiser.com/developer-document/rest-api/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete UK Address](actions/autocomplete-uk-address.md) | `GET /autoc/json/:maf` | [docs](https://www.hopewiser.com/developer-document/autocomplete-rest-api/) |
| [Get Autocomplete Service Versions](actions/get-autocomplete-service-versions.md) | `GET /autoc/json/:maf` | [docs](https://www.hopewiser.com/developer-document/autocomplete-rest-api/) |
| [Get Autocomplete UK Address By SID](actions/get-autocomplete-uk-address-by-sid.md) | `GET /autoc/json/:maf` | [docs](https://www.hopewiser.com/developer-document/autocomplete-rest-api/) |
| [Get UK Address By SID](actions/get-uk-address-by-sid.md) | `GET /atlaslive/json/:maf` | [docs](https://www.hopewiser.com/developer-document/rest-api/) |
| [Get UK Address Service Versions](actions/get-uk-address-service-versions.md) | `GET /atlaslive/json/:maf` | [docs](https://www.hopewiser.com/developer-document/rest-api/) |
| [List Autocomplete Master Address Files](actions/list-autocomplete-master-address-files.md) | `GET /autoc/json` | [docs](https://www.hopewiser.com/developer-document/autocomplete-rest-api/) |
| [List Autocomplete Output Fields](actions/list-autocomplete-output-fields.md) | `GET /autoc/json/:maf` | [docs](https://www.hopewiser.com/developer-document/autocomplete-rest-api/) |
| [List International Countries](actions/list-international-countries.md) | `GET /atlaslive/countries/json` | [docs](https://www.hopewiser.com/developer-document/international-rest-api/) |
| [List Master Address Files](actions/list-master-address-files.md) | `GET /atlaslive/json` | [docs](https://www.hopewiser.com/developer-document/rest-api/) |
| [List UK Address Output Fields](actions/list-uk-address-output-fields.md) | `GET /atlaslive/json/:maf` | [docs](https://www.hopewiser.com/developer-document/rest-api/) |
| [List UK Address Search Indexes](actions/list-uk-address-search-indexes.md) | `GET /atlaslive/json/:maf` | [docs](https://www.hopewiser.com/developer-document/rest-api/) |
| [Search UK Address](actions/search-uk-address.md) | `GET /atlaslive/json/:maf` | [docs](https://www.hopewiser.com/developer-document/rest-api/) |
