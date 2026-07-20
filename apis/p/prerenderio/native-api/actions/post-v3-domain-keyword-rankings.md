# Create Domain Keyword Rankings with Prerender.io

Creates a domain keyword ranking in Prerender.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/domain-keyword-rankings`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [Create Domain Keyword Rankings](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domain` | body | `string` | yes |
| `keywords` | body | `list<string>` | no |
