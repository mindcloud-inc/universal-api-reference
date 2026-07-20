# Create Sitemap Crawl with Prerender.io

Starts a sitemap crawl in Prerender.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/sitemap/{id}/crawl`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [Create Sitemap Crawl](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `adaptiveType` | body | `string` | no |
| `id` | path | `number` | yes |
| `recacheAll` | body | `boolean` | yes |
