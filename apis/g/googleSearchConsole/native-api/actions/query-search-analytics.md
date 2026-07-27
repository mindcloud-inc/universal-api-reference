# Query Search Analytics with Google Search Console

## Endpoint

- **Method:** `POST`
- **Path:** `sites/:siteUrl/searchAnalytics/query`
- **Base URL:** `https://www.googleapis.com/webmasters/v3`
- **Official documentation:** [Query Search Analytics](https://developers.google.com/webmaster-tools/v1/searchanalytics/query)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteUrl` | path | `list<string>` | yes | The Search Console property URL to query, such as a URL-prefix property or a sc-domain property. |
| `startDate` | body | `date` | yes | Start date of the requested date range in YYYY-MM-DD format, in Pacific Time. |
| `endDate` | body | `date` | yes | End date of the requested date range in YYYY-MM-DD format, in Pacific Time. |
| `dimensions[]` | body | `array<string>` | no | Optional list of dimensions to group rows by, such as country, device, page, query, date, or hour. |
| `type` | body | `list<string>` | no | Optional search result type filter. Docs list web, image, video, news, googleNews, and discover. Accepted values: `discover`, `googleNews`, `image`, `news`, `video`, `web`. |
| `dimensionFilterGroups[]` | body | `array<object>` | no | Optional dimension filter groups payload matching the Search Analytics API request body format. |
| `aggregationType` | body | `list<string>` | no | Optional aggregation type. Docs list auto, byPage, byProperty, and byNewsShowcasePanel with scope restrictions. Accepted values: `auto`, `byNewsShowcasePanel`, `byPage`, `byProperty`. |
| `dataState` | body | `list<string>` | no | Optional data freshness mode. Docs list final, all, and hourly_all. Accepted values: `all`, `final`, `hourly_all`. |
