# Centers for Disease Control and Prevention: Native API Reference

A consolidated summary of Centers for Disease Control and Prevention's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://tools.cdc.gov/api/docs/info.aspx
- **API base URL:** `https://tools.cdc.gov/api`

## Authentication

### No authentication

CDC Content Services API endpoints used by this app are publicly accessible.

This API does not require request authentication.

[Official authentication documentation](https://tools.cdc.gov/api/docs/info.aspx)

## API conventions

Responses from this API use JSON. Response data is read from `results`. The next-page cursor is read from `meta.pagination.nextUrl`. The total page count is read from `meta.pagination.totalPages`. The current page number is read from `meta.pagination.pageNum`.

## Pagination

Use `max` in the query string to set the page size (default 8; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `ASC` for ascending order and `DESC` for descending order. Multiple sort fields can be combined.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Media](actions/get-media.md) | `GET /v2/resources/media/:mediaId` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [Get Media Content](actions/get-media-content.md) | `GET /v2/resources/media/:mediaId/content` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [Get Media Embed Code](actions/get-media-embed-code.md) | `GET /v2/resources/media/:mediaId/embed` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [Get Media Syndicated HTML](actions/get-media-syndicated-html.md) | `GET /v2/resources/media/:mediaId/syndicate` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [Get Tag](actions/get-tag.md) | `GET /v2/resources/tags/:tagId` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Audiences](actions/list-audiences.md) | `GET /v2/resources/audiences` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Languages](actions/list-languages.md) | `GET /v2/resources/languages` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Media By Tag](actions/list-media-by-tag.md) | `GET /v2/resources/tags/:tagId/media` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Media Types](actions/list-media-types.md) | `GET /v2/resources/mediatypes` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Organization Types](actions/list-organization-types.md) | `GET /v2/resources/organizationtypes` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Organizations](actions/list-organizations.md) | `GET /v2/resources/organizations` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Related Tags](actions/list-related-tags.md) | `GET /v2/resources/tags/:tagId/related` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Sources](actions/list-sources.md) | `GET /v2/resources/sources` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Tag Types](actions/list-tag-types.md) | `GET /v2/resources/tagtypes` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Tags](actions/list-tags.md) | `GET /v2/resources/tags` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Topics](actions/list-topics.md) | `GET /v2/resources/topics` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [Search Media](actions/search-media.md) | `GET /v2/resources/media` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
