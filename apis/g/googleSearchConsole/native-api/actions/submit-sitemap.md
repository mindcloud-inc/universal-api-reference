# Submit Sitemap with Google Search Console

## Endpoint

- **Method:** `PUT`
- **Path:** `sites/:siteUrl/sitemaps/:feedpath`
- **Base URL:** `https://www.googleapis.com/webmasters/v3`
- **Official documentation:** [Submit Sitemap](https://developers.google.com/webmaster-tools/v1/sitemaps/submit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteUrl` | path | `list<string>` | yes | The Search Console property URL that owns the sitemap. |
| `feedpath` | path | `string` | yes | The full URL of the sitemap to submit, for example https://www.example.com/sitemap.xml. |
