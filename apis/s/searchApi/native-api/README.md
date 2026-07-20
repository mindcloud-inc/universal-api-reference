# SearchApi: Native API Reference

A consolidated summary of SearchApi's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.searchapi.io/docs/google
- **OpenAPI specification:** https://www.searchapi.io/openapi/google.yaml
- **API base URL:** `https://www.searchapi.io/api/v1`

## Authentication

### API Key

Authenticate with a SearchApi API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.searchapi.io/docs/account-api)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | `GET /me` | [docs](https://www.searchapi.io/docs/account-api) |
| [Get Autocomplete Suggestions](actions/get-autocomplete-suggestions.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-autocomplete) |
| [Get Directions](actions/get-directions.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-maps-directions-api) |
| [Get Map Photos](actions/get-map-photos.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-maps-photos) |
| [Get Map Place](actions/get-map-place.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-maps-place) |
| [Get Map Reviews](actions/get-map-reviews.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-maps-reviews) |
| [Get Product](actions/get-product.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-product) |
| [Get Product Offers](actions/get-product-offers.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-product-offers) |
| [Get Product Reviews](actions/get-product-reviews.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-product-reviews) |
| [Get Product Specs](actions/get-product-specs.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-product-specifications) |
| [Search Finance](actions/search-finance.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-finance) |
| [Search Flights](actions/search-flights.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-flights-api) |
| [Search Forums](actions/search-forums.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-forums-api) |
| [Search Hotels](actions/search-hotels.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-hotels-api) |
| [Search Images](actions/search-images.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-images) |
| [Search Jobs](actions/search-jobs.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-jobs) |
| [Search Maps](actions/search-maps.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-maps) |
| [Search News](actions/search-news.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-news) |
| [Search Patents](actions/search-patents.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-patents) |
| [Search Scholar](actions/search-scholar.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-scholar) |
| [Search Shopping](actions/search-shopping.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-shopping) |
| [Search Trends](actions/search-trends.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-trends) |
| [Search Videos](actions/search-videos.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google-videos) |
| [Search Web](actions/search-web.md) | `GET /search` | [docs](https://www.searchapi.io/docs/google) |
