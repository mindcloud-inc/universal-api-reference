# Library of Congress: Native API Reference

A consolidated summary of Library of Congress's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://www.loc.gov/apis/json-and-yaml/
- **API base URL:** `https://www.loc.gov`

## Authentication

### No Authentication

The official loc.gov JSON/YAML API is public and does not require provider-managed credentials for the documented build path.

This API does not require request authentication.

[Official authentication documentation](https://www.loc.gov/apis/json-and-yaml/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Accept-Language` | `en-US,en;q=0.9` |
| `User-Agent` | `Mozilla/5.0 (compatible; MindCloud LibraryOfCongress integration validation)` |

Responses from this API use JSON.

## Pagination

Use `c` in the query string to set the page size (default 25; accepted range 1–1000). Use `sp` in the query string to choose the page; numbering starts at 1.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Collection](actions/get-collection.md) | `GET /collections/{collectionSlug}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Collection Facets](actions/get-collection-facets.md) | `GET /collections/{collectionSlug}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Collection Pagination](actions/get-collection-pagination.md) | `GET /collections/{collectionSlug}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Collection Results](actions/get-collection-results.md) | `GET /collections/{collectionSlug}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Item](actions/get-item.md) | `GET /item/{itemId}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Item Citation](actions/get-item-citation.md) | `GET /item/{itemId}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Item Metadata](actions/get-item-metadata.md) | `GET /item/{itemId}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Item Resources](actions/get-item-resources.md) | `GET /item/{itemId}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Resource](actions/get-resource.md) | `GET /resource/{resourceId}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Resource Citation](actions/get-resource-citation.md) | `GET /resource/{resourceId}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Resource Details](actions/get-resource-details.md) | `GET /resource/{resourceId}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Resource Page](actions/get-resource-page.md) | `GET /resource/{resourceId}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Resource Related Resources](actions/get-resource-related-resources.md) | `GET /resource/{resourceId}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Get Resource Segments](actions/get-resource-segments.md) | `GET /resource/{resourceId}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [List Collections](actions/list-collections.md) | `GET /collections/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Search All Content](actions/search-all-content.md) | `GET /search/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Search Audio Recordings](actions/search-audio-recordings.md) | `GET /audio/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Search Books](actions/search-books.md) | `GET /books/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Search Collection Items](actions/search-collection-items.md) | `GET /collections/{collectionSlug}/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Search Film and Videos](actions/search-film-and-videos.md) | `GET /film-and-videos/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Search Manuscripts](actions/search-manuscripts.md) | `GET /manuscripts/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Search Maps](actions/search-maps.md) | `GET /maps/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Search Newspapers](actions/search-newspapers.md) | `GET /newspapers/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Search Notated Music](actions/search-notated-music.md) | `GET /notated-music/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Search Periodicals](actions/search-periodicals.md) | `GET /search/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/parameters/) |
| [Search Personal Narratives](actions/search-personal-narratives.md) | `GET /search/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/parameters/) |
| [Search Photos](actions/search-photos.md) | `GET /photos/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Search Software and E-Resources](actions/search-software-and-e-resources.md) | `GET /search/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/parameters/) |
| [Search Sound Recordings](actions/search-sound-recordings.md) | `GET /search/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/parameters/) |
| [Search Web Archives](actions/search-web-archives.md) | `GET /web-archives/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/) |
| [Search 3D Objects](actions/search3d-objects.md) | `GET /search/` | [docs](https://www.loc.gov/apis/json-and-yaml/requests/parameters/) |
