# Short.io: Native API Reference

A consolidated summary of Short.io's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://developers.short.io/reference
- **API base URL:** `https://api.short.io`

## Authentication

### API Key

Authenticate with a Short.io secret API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.short.io/docs/creating-an-api-key)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `limit` in the query string to set the page size (maximum 149).

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Single Tag to Links in Bulk](actions/add-single-tag-to-links-in-bulk.md) | `POST /tags/bulk` | [docs](https://developers.short.io/reference/post_tags-bulk) |
| [Archive Link](actions/archive-link.md) | `POST /links/archive` | [docs](https://developers.short.io/reference/post_links-archive) |
| [Archive Links in Bulk](actions/archive-links-in-bulk.md) | `POST /links/archive_bulk` | [docs](https://developers.short.io/reference/post_links-archive-bulk) |
| [Create Domain](actions/create-domain.md) | `POST /domains` | [docs](https://developers.short.io/reference/post_domains) |
| [Create Link](actions/create-link.md) | `POST /links` | [docs](https://developers.short.io/reference/post_links) |
| [Delete Link](actions/delete-link.md) | `DELETE /links/:linkId` | [docs](https://developers.short.io/reference/delete_links-link-id) |
| [Delete Links in Bulk](actions/delete-links-in-bulk.md) | `DELETE /links/delete_bulk` | [docs](https://developers.short.io/reference/delete_links-delete-bulk) |
| [Get Domain](actions/get-domain.md) | `GET /domains/:domainId` | [docs](https://developers.short.io/reference/get_domains-domainid) |
| [Get Domain Statistics](actions/get-domain-statistics.md) | `GET https://statistics.short.io/statistics/domain/:domainId` | [docs](https://developers.short.io/v1.2/reference/getdomaindomainid) |
| [Get Link](actions/get-link.md) | `GET /links/:linkId` | [docs](https://developers.short.io/reference/get_links-linkid) |
| [Get Link by Path](actions/get-link-by-path.md) | `GET /links/expand` | [docs](https://developers.short.io/reference/get_links-expand) |
| [Get Link Clicks By IDs](actions/get-link-clicks-by-i-ds.md) | `GET https://statistics.short.io/statistics/domain/:domainId/link_clicks` | [docs](https://developers.short.io/v1.2/reference/getdomaindomainidlink_clicks) |
| [Get Link Clicks By Paths](actions/get-link-clicks-by-paths.md) | `POST https://statistics.short.io/statistics/domain/:domainId/link_clicks` | [docs](https://developers.short.io/v1.2/reference/postdomaindomainidlink_clicks) |
| [Get Link Regions](actions/get-link-regions.md) | `GET /link_region/:linkId` | [docs](https://developers.short.io/reference/get_link-region-linkid) |
| [Get Link Statistics](actions/get-link-statistics.md) | `GET https://statistics.short.io/statistics/link/:linkId` | [docs](https://developers.short.io/v1.2/reference/getlinklinkid) |
| [List Domains](actions/list-domains.md) | `GET /api/domains` | [docs](https://developers.short.io/reference/get_api-domains) |
| [List Links](actions/list-links.md) | `GET /api/links` | [docs](https://developers.short.io/reference/get_api-links) |
| [List Links by Original URL](actions/list-links-by-original-url.md) | `GET /links/multiple-by-url` | [docs](https://developers.short.io/reference/get_links-multiple-by-url) |
| [Unarchive Link](actions/unarchive-link.md) | `POST /links/unarchive` | [docs](https://developers.short.io/reference/post_links-unarchive) |
| [Unarchive Links in Bulk](actions/unarchive-links-in-bulk.md) | `POST /links/unarchive_bulk` | [docs](https://developers.short.io/reference/post_links-unarchive-bulk) |
| [Update Link](actions/update-link.md) | `POST /links/:linkId` | [docs](https://developers.short.io/reference/post_links-linkid) |
