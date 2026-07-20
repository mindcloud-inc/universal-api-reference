# Create Sitemap with Prerender.io

Creates a sitemap entry in Prerender.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/sitemap`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [Create Sitemap](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `adaptiveType` | body | `string` | no |
| `isIntegrationFlow` | body | `boolean` | yes |
| `recacheAll` | body | `boolean` | yes |
| `revisitInterval` | body | `number` | yes |
| `url` | body | `string` | yes |
