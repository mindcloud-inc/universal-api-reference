# Get Domains Last Cached Urls with Prerender.io

Retrieves a domain's last cached URLs from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/domains/{domain}/last-cached-urls`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [Get Domains Last Cached Urls](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domain` | path | `string` | yes |
| `page` | query | `number` | yes |
