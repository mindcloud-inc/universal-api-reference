# Get Sitemap with Google Search Console

## Endpoint

- **Method:** `GET`
- **Path:** `sites/:siteUrl/sitemaps/:feedpath`
- **Base URL:** `https://www.googleapis.com/webmasters/v3`
- **Official documentation:** [Get Sitemap](https://developers.google.com/webmaster-tools/v1/sitemaps/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteUrl` | path | `list<string>` | yes | The Search Console property URL that owns the sitemap. |
| `feedpath` | path | `string` | yes | The full URL of the sitemap to retrieve, for example https://www.example.com/sitemap.xml. |
