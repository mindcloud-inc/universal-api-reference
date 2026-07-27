# List Sitemaps with Google Search Console

## Endpoint

- **Method:** `GET`
- **Path:** `sites/:siteUrl/sitemaps`
- **Base URL:** `https://www.googleapis.com/webmasters/v3`
- **Official documentation:** [List Sitemaps](https://developers.google.com/webmaster-tools/v1/sitemaps/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteUrl` | path | `list<string>` | yes | The Search Console property URL whose submitted sitemaps you want to list. |
| `sitemapIndex` | query | `string` | no | Optional sitemap index URL to limit the results to the entries included in that sitemap index. |
