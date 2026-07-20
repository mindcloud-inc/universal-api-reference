# Update Sitemap with Prerender.io

Updates a sitemap entry in Prerender.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v3/sitemap/{id}`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [Update Sitemap](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `adaptiveType` | body | `string` | no |
| `enabled` | body | `boolean` | no |
| `id` | path | `number` | yes |
| `revisitInterval` | body | `number` | no |
