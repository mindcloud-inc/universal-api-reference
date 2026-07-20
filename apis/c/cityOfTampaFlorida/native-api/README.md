# City of Tampa, Florida: Native API Reference

A consolidated summary of City of Tampa, Florida's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.tampa.gov/info/rss-feeds
- **API base URL:** `https://www.tampa.gov`

## Authentication

### No Authentication

This API does not require request authentication.

[Official authentication documentation](https://www.tampa.gov/info/rss-feeds)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Collection](actions/get-collection.md) | `GET https://city-tampa.opendata.arcgis.com/api/search/v1/collections/:collectionId` | [docs](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json) |
| [Get Collection Aggregations](actions/get-collection-aggregations.md) | `GET https://city-tampa.opendata.arcgis.com/api/search/v1/collections/:collectionId/aggregations` | [docs](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json) |
| [Get Collection Item](actions/get-collection-item.md) | `GET https://city-tampa.opendata.arcgis.com/api/search/v1/collections/:collectionId/items/:itemId` | [docs](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json) |
| [Get Collection Queryables](actions/get-collection-queryables.md) | `GET https://city-tampa.opendata.arcgis.com/api/search/v1/collections/:collectionId/queryables` | [docs](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json) |
| [Get Search API Conformance](actions/get-search-api-conformance.md) | `GET https://city-tampa.opendata.arcgis.com/api/search/v1/conformance` | [docs](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json) |
| [Get Search Catalog](actions/get-search-catalog.md) | `GET https://city-tampa.opendata.arcgis.com/api/search/v1/catalog` | [docs](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json) |
| [List All Events](actions/list-all-events.md) | `GET /mobile-feeds/events/all` | [docs](https://www.tampa.gov/info/rss-feeds) |
| [List Calendar Feed Items](actions/list-calendar-feed-items.md) | `GET /calendar/rss.xml` | [docs](https://www.tampa.gov/info/rss-feeds) |
| [List Collection Items](actions/list-collection-items.md) | `GET https://city-tampa.opendata.arcgis.com/api/search/v1/collections/:collectionId/items` | [docs](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json) |
| [List Connected Records](actions/list-connected-records.md) | `GET https://city-tampa.opendata.arcgis.com/api/search/v1/collections/:collectionId/items/:recordId/connected` | [docs](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json) |
| [List Construction Project News Feed Items](actions/list-construction-project-news-feed-items.md) | `GET /news/feed/cpb` | [docs](https://www.tampa.gov/info/rss-feeds) |
| [List Contract Administration News Feed Items](actions/list-contract-administration-news-feed-items.md) | `GET /news/feed/rfqs` | [docs](https://www.tampa.gov/info/rss-feeds) |
| [List Data Collections](actions/list-data-collections.md) | `GET https://city-tampa.opendata.arcgis.com/api/search/v1/collections` | [docs](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json) |
| [List Event Types](actions/list-event-types.md) | `GET /taxonomy/terms/calendar_type` | [docs](https://www.tampa.gov/info/rss-feeds) |
| [List Events By Type](actions/list-events-by-type.md) | `GET /mobile-feeds/events/:typeId` | [docs](https://www.tampa.gov/info/rss-feeds) |
| [List Job Openings](actions/list-job-openings.md) | `GET https://jobapscloud.com/Tampa/rss.asp` | [docs](https://www.tampa.gov/info/rss-feeds) |
| [List News Feed Items](actions/list-news-feed-items.md) | `GET /news/feed` | [docs](https://www.tampa.gov/info/rss-feeds) |
| [List Police Events](actions/list-police-events.md) | `GET /feeds/police-calendar-all` | [docs](https://www.tampa.gov/info/rss-feeds) |
| [List Police News Feed Items](actions/list-police-news-feed-items.md) | `GET /news/feed/police` | [docs](https://www.tampa.gov/info/rss-feeds) |
| [List Related Records](actions/list-related-records.md) | `GET https://city-tampa.opendata.arcgis.com/api/search/v1/collections/:collectionId/items/:recordId/related` | [docs](https://city-tampa.opendata.arcgis.com/api/search/definition/?f=json) |
