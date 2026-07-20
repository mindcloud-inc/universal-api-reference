# CDC Content Services: Native API Reference

A consolidated summary of CDC Content Services's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://tools.cdc.gov/api/docs/info.aspx
- **API base URL:** `https://tools.cdc.gov/api`

## Authentication

### No authentication

The CDC Content Services API is publicly accessible and does not require credentials for documented read endpoints.

This API does not require request authentication.

[Official authentication documentation](https://tools.cdc.gov/api/docs/info.aspx)

## API conventions

Responses from this API use JSON. The next-page cursor is read from `meta.pagination.nextUrl`. The total page count is read from `meta.pagination.totalPages`. The current page number is read from `meta.pagination.pageNum`.

## Pagination

Use `max` in the query string to set the page size (default 100; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`.

## Sorting

Set the sort field with `sort` in the query string. Use `ascending` for ascending order and `-` for descending order. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Media](actions/get-media.md) | `GET /v2/resources/media/[:mediaId]` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [Get Media Content](actions/get-media-content.md) | `GET /v2/resources/media/[:mediaId]/content` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [Get Media Embed Code](actions/get-media-embed-code.md) | `GET /v2/resources/media/[:mediaId]/embed` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [Get Media Syndication](actions/get-media-syndication.md) | `GET /v2/resources/media/[:mediaId]/syndicate` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [Get Tag](actions/get-tag.md) | `GET /v2/resources/tags/[:tagId]` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Audiences](actions/list-audiences.md) | `GET /v2/resources/audiences` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Languages](actions/list-languages.md) | `GET /v2/resources/languages` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Media](actions/list-media.md) | `GET /v2/resources/media` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Media By Tag](actions/list-media-by-tag.md) | `GET /v2/resources/tags/[:tagId]/media` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Media Types](actions/list-media-types.md) | `GET /v2/resources/mediatypes` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Organization Types](actions/list-organization-types.md) | `GET /v2/resources/organizationtypes` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Organizations](actions/list-organizations.md) | `GET /v2/resources/organizations` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Related Tags](actions/list-related-tags.md) | `GET /v2/resources/tags/[:tagId]/related` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Sources](actions/list-sources.md) | `GET /v2/resources/sources` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Tag Types](actions/list-tag-types.md) | `GET /v2/resources/tagtypes` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Tags](actions/list-tags.md) | `GET /v2/resources/tags` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
| [List Topics](actions/list-topics.md) | `GET /v2/resources/topics` | [docs](https://tools.cdc.gov/api/docs/info.aspx) |
