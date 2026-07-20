# Active Network: Native API Reference

A consolidated summary of Active Network's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://developer.active.com/docs
- **API base URL:** `http://api.amp.active.com`

## Authentication

### API Key

Use an ACTIVE developer key for the public Activity Search API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.active.com/docs/read/v2_Activity_API_Search)

## Pagination

Use `per_page` in the query string to set the page size (default 25; minimum 1). Use `current_page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Asset By Exact Name](actions/get-asset-by-exact-name.md) | `GET /v2/search` | [docs](https://developer.active.com/docs/read/v2_Activity_API_Search) |
| [Get Asset By Guid](actions/get-asset-by-guid.md) | `GET /v2/search` | [docs](https://developer.active.com/docs/read/v2_Activity_API_Search) |
| [Get Campground Details](actions/get-campground-details.md) | `GET /camping/campground/details` | [docs](https://developer.active.com/docs/read/Campground_Details_API) |
| [List Activity Categories](actions/list-activity-categories.md) | `GET /v2/search` | [docs](https://developer.active.com/docs/read/v2_Activity_API_Search) |
| [List Activity Topics](actions/list-activity-topics.md) | `GET /v2/search` | [docs](https://developer.active.com/docs/read/v2_Activity_API_Search) |
| [Search Assets](actions/search-assets.md) | `GET /v2/search` | [docs](https://developer.active.com/docs/read/v2_Activity_API_Search) |
| [Search Campgrounds](actions/search-campgrounds.md) | `GET /camping/campgrounds/` | [docs](https://developer.active.com/docs/read/Campground_Search_API) |
| [Search Campsites](actions/search-campsites.md) | `GET /camping/campsites/` | [docs](https://developer.active.com/docs/read/Campsite_Search_API) |
| [Search Kids Assets](actions/search-kids-assets.md) | `GET /v2/search` | [docs](https://developer.active.com/docs/read/Kids_Activity_Search_API_v2) |
