# OMDb: Native API Reference

A consolidated summary of OMDb's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://www.omdbapi.com
- **OpenAPI specification:** https://www.omdbapi.com/swagger.json
- **API base URL:** `https://www.omdbapi.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.omdbapi.com/apikey.aspx)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Episode by IMDb ID](actions/get-episode-by-imdb-id.md) | `GET /` | [docs](https://www.omdbapi.com) |
| [Get Episode by Series Title](actions/get-episode-by-series-title.md) | `GET /` | [docs](https://www.omdbapi.com) |
| [Get Movie by Title](actions/get-movie-by-title.md) | `GET /` | [docs](https://www.omdbapi.com) |
| [Get Season by IMDb ID](actions/get-season-by-imdb-id.md) | `GET /` | [docs](https://www.omdbapi.com) |
| [Get Season by Series Title](actions/get-season-by-series-title.md) | `GET /` | [docs](https://www.omdbapi.com) |
| [Get Series by Title](actions/get-series-by-title.md) | `GET /` | [docs](https://www.omdbapi.com) |
| [Get Title by IMDb ID](actions/get-title-by-imdb-id.md) | `GET /` | [docs](https://www.omdbapi.com) |
| [Get Title by Title](actions/get-title-by-title.md) | `GET /` | [docs](https://www.omdbapi.com) |
| [Search Movies](actions/search-movies.md) | `GET /` | [docs](https://www.omdbapi.com) |
| [Search Series](actions/search-series.md) | `GET /` | [docs](https://www.omdbapi.com) |
| [Search Titles](actions/search-titles.md) | `GET /` | [docs](https://www.omdbapi.com) |
