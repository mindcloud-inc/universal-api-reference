# Update Domain Keyword Rankings with Prerender.io

Updates a domain keyword ranking in Prerender.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/domain-keyword-rankings/{id}`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [Update Domain Keyword Rankings](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `keywords` | body | `list<string>` | yes |
